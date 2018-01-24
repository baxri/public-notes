
# PM2

Source: [Documentation](http://pm2.keymetrics.io/docs/usage/application-declaration/#javascript-format)

## Process File (ecosystem)

To generate a sample process file you can type this command:

`pm2 ecosystem`

This will generate a sample, ecosystem.config.js.
To generate a ecosystem file without any comment just run.

`pm2 ecosystem simple`

### JSON format

The configuration can also be in JSON format.

`{
  "apps" : [{
    "name"        : "worker",
    "script"      : "./worker.js",
    "watch"       : true,
    "env": {
      "NODE_ENV": "development"
    },
    "env_production" : {
       "NODE_ENV": "production"
    }
  },{
    "name"       : "api-app",
    "script"     : "./api.js",
    "instances"  : 4,
    "exec_mode"  : "cluster"
  }]
}`

Then you can run and manage your processes easily:

Start all applications

`pm2 start ecosystem.config.js`

Start only the app named worker-app

`pm2 start ecosystem.config.js --only worker-app`

Stop all

`pm2 stop ecosystem.config.js`

Restart all

`pm2 restart ecosystem.config.js`

Delete all

`pm2 delete ecosystem.config.js`

### Act on a specific process

You can also act on a particular application by using its name and the option --only <app_name>:

`pm2 start   ecosystem.config.js --only api-app`





