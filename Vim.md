=======
[[VimPlugins]]

以下命令可以对标点内的内容进行操作。
ci'、ci"、ci(、ci[、ci{、ci< - 分别更改这些配对标点符号中的文本内容
di'、di"、di(或dib、di[、di{或diB、di< - 分别删除这些配对标点符号中的文本内容
yi'、yi"、yi(、yi[、yi{、yi< - 分别复制这些配对标点符号中的文本内容
vi'、vi"、vi(、vi[、vi{、vi< - 分别选中这些配对标点符号中的文本内容

另外如果把上面的i改成a可以连配对标点一起操作。

Open multiple files in tab
vim -p file1 file2 file3

vim ./* opens files in the folder except in another directory

FuzzyFinder
打开vim/vim72/autoload/fuf/file.vim，找到function fuf#file#onInit()，增加一行：

call fuf#defineLaunchCommand(‘FufFileRecursive’, s:MODE_NAME, ‘”**/”‘)

然后定义快捷键，在_vimrc中增加：

” FuzzyFinder – Ctrl + Shift + R
map <C-S-R> :FufFileRecursive<CR>

这样，在vim中，按下Ctrl+Shift+R，就可以快速查找文件了。
