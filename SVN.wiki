=SVN=
==Tips==
===svn ignore===
下文以.git文件夹为例。

若想创建了一个文件夹，并且把它加入版本控制，但忽略文件夹中的所有文件的内容：
{{{
$ svn mkdir .git
$ svn propset svn:ignore '*' .git
$ svn ci -m 'Adding ".git" and ignoring its contents.'
}}}
若想创建一个文件夹，但不加入版本控制，即忽略这个文件夹。
*注意第二行的后面的点号，表示将该目录的所有文件*：
{{{
$ mkdir .git
$ svn propset svn:ignore '.git' .
$ svn ci -m 'Ignoring a directory called ".git".'
}}}
若已经创建了文件夹，并加入了版本控制，现在想忽略这个文件夹，但要保持文件夹的内容：
{{{
$ svn export .git .git-tmp
$ svn rm .git
$ svn ci -m 'Removing inadvertently added directory ".git".'
$ mv .git-tmp .git
$ svn propset svn:ignore '.git' .
$ svn ci -m 'Ignoring a directory called ".git".'
}}}
===svn cleanup===
删除.svn目录
{{{
find . -type d -name ".svn"|xargs rm -rf
}}}
