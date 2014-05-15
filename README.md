remote_syslog Docker container
==============================

To get logs from your machine to a remote syslog daemon using [remote_syslog](https://github.com/papertrail/remote_syslog)

For example, we are forwarding our nginx reverse proxy logs to papertrail using these commands:

```
docker run -d -v=/var/log/nginx/access.log:/access.log  octohost/remote_syslog  -p xxxxx -d logs.papertrailapp.com /access.log

docker run -d -v=/var/log/nginx/error.log:/error.log  octohost/remote_syslog  -p xxxxx -d logs.papertrailapp.com /error.log
```

You can pull an already built version: `docker pull octohost/remote_syslog`

Thanks to [Papertrail](http://papertrailapp.com) for making the gem available.
