heroku-buildpack-geoip-lib-and-db
======================

This should be used with https://github.com/ddollar/heroku-buildpack-multi

It downloads the GeopIP db from Maxmind. If you use this in conjunction with  [maxmind_geoip2](https://github.com/envato/geoip2)
 gem, you can avoid using services like freegeoip which limits your queries.

You can add it to upcoming builds of an existing application:
```
$ heroku config:add BUILDPACK_URL=https://github.com/ddollar/heroku-buildpack-multi.git
```
Then add a .buildpack
```
https://github.com/monkseal/heroku-buildpack-geoip-lib-and-db
https://github.com/heroku/heroku-buildpack-ruby
```
### Testing locally

To run the script and test locally:
```
mkdir -p build cache env
./bin/compile build cache env
``` 
