# Strapi test instance

The instance is live on : https://strapi-ods-heroku.herokuapp.com/
See the notion for admin access or ask me.

To tweak models, configs etc. you need to do it locally and then upload your changes to heroku, which will update the model. 
```
git clone https://github.com/etienneburdet/strapi-ods-heroku.git
cd strapi-ods-heroku
yarn //or npm install
git checkout -b my-tweak
strapi dev // now live on https://localhost:1337/
```
And you have a working copy locally. Create everything in Strapi GUI, commit changes, merge branch (PR or git merge).
🚨**Please don't dev on master as it is the source of truth for Heroku deploys** 🚨

Then create an Heroku account, ask to be invited on the heroku project and : 
```
brew tap heroku/brew && brew install heroku
heroku login
heroku git:remote -a strapi-ods-heroku
git push heroku master
```
Your change on the model should be live ! You can/edit content and export the API endpoint to ODS !
