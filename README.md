heroku-buildpack-geoip-db-only
======================

This should be used with https://github.com/ddollar/heroku-buildpack-multi

It downloads the GeopIP db from Maxmind. If you use this in conjunction with  [maxminddb](https://github.com/yhirose/maxminddb)
 gem, you can avoid using services like freegeoip which limits your queries.

You can add it to upcoming builds of an existing application:
```
$ heroku config:add BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi.git
```
Then add a .buildpack
```
https://github.com/monkseal/heroku-buildpack-geoip-db-only
https://github.com/heroku/heroku-buildpack-ruby
```
