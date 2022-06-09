# EasyExample Call Server - NodeJS

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/ZEGOCLOUD/room_list_server_nodejs)


This is an example of a server program for "querying the room list under your appid"

Notice
1. This function needs to contact us to activate it to use
2. Since this function has a QPS limit of 20/s, we have made a simple 500ms cache logic in the example


## Getting started

### Create ZEGOCLOUD project

Create project on [ZEGOCLOUD Console](https://console.zegocloud.com), then get the required info as shown below:

- Get your AppID from ZEGOCLOUD Console [My Projects](https://console.zegocloud.com/project)

- Get your ServerSecret from ZEGOCLOUD Console [My Projects -> project's Edit -> Basic Configurations](https://console.zegocloud.com/project)

### Deploy service

1. Click this deploy button at the top of this page to start deploy your service.

![](docs/images/deploy_to_heroku.jpg)

2. Pick your Heroku app-name and fill in the input box.
3. Open the `Firebase Admin SDK Private Key` you just obtain at the above step, and fill in the content to the `Config Vars` parameter input box.
4. Press `Deploy App` button, wait for the depoly process completed.
5. Once done you will get an url for your instance, try accessing `https://<heroku url>/access_token?uid=1234` to check if it works.

## Note

Token valid in 3600 seconds by default. If you want to change the expired time, request with the `expired_ts` parameter. e.g. `https://<heroku url>/access_token?uid=1234&expired_ts=7200`

## About us

https://www.zegocloud.com/

## License
The MIT License (MIT).
