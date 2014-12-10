dxc4.com welcome page
========

THe welcome page for dxc4.com, describing the dxc4 chess API available at http://api.dxc4.com with links to the demo and domumentation.


Set up
=========

install dependencies:

(requires ruby for sass gem and node/npm)

```sh
npm install
npm install bower -g
bower install
gem install sass
```

build into dist folder:
```sh
gulp
```

Start server
==========

```sh
export CHESS_INDEX_PORT=80
node server.js
```

PM2 
=========

You can use PM2 to run the API which sports better logging, auto restarts, etc.. 
https://github.com/Unitech/PM2

Caveat: PM2 does not pass through enviroment variables so you will require to use a JSON config file like this:

```json
{
    "name"        : "Chess Welcome Page",
    "script"      : "server.js",
    "log_date_format"  : "YYYY-MM-DD HH:mm Z",
    "env": {
        "CHESS_INDEX_PORT": 80
    }
}
```
