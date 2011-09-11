=Heroku Guide=
==Deploy==
Write the app, and don't forget to change the listening port using the following code
{{{
  var port = process.env.PORT || 3000;
  app.listen(port, function() {
      console.log("Listening on " + port);
  });
}}}

Declare Dependencies With NPM, need to add global modules like express

Ignore the node_module folder in git

Create a file name `Profile` with following content:
{{{
  web: node app.js
}}}

Create app 
{{{
  heroku create --stack cedar
  git push heroku master
}}}


==App Rename==
After rename the app, the git remote need to change accordingly
{{{
heroku rename newname
}}}
Or change it from the web and update the git remote
{{{
git remote rm heroku
git remote add heroku git@heroku.com:newname.git
}}}

==Logs==
{{{
  heroku logs 
}}}
