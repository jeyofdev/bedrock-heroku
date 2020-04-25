# Deploy wordpress site with heroku


## Requirements

* PHP >= 7.1
* Composer - [Install](https://getcomposer.org/download/)
* Heroku CLI - [Install](https://devcenter.heroku.com/articles/heroku-cli)



## Install wordpress with Bedrock
```sh
$ cd yourprojectfolder
$ composer create-project roots/bedrock
```

## Deploy the application
create a Heroku app
```sh
$ heroku create your-project-name --region eu
```

Link the github account via the deploy tab of heroku. 

See heroku [doc](https://devcenter.heroku.com/articles/github-integration).

Set environment variables. See heroku [doc](https://devcenter.heroku.com/articles/config-vars).

List of variables :

* AUTH_KEY
* AUTH_SALT
* LOGGED_IN_KEY
* LOGGED_IN_SALT
* NONCE_KEY
* NONCE_SALT
* SECURE_AUTH_KEY
* SECURE_AUTH_SALT
* DATABASE_URL (ex : `mysql://user:password@host/database?reconnect=true`)
* WP_HOME (ex : `https://example.com/`)
* WP_SITEURL (ex : `https://example.com/wp`)

Generate the first 8 variables via this [link](https://api.wordpress.org/secret-key/1.1/salt/)