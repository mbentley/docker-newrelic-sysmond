mbentley/newrelic-sysmond
=========================

docker image for New Relic's server monitoring agent - sysmond
based off of debian:jessie

To pull this image:
`docker pull mbentley/newrelic-sysmond`

Example usage:

```
docker run -d --net=host --name newrelic-sysmond \
  -e NEW_RELIC_LICENSE_KEY=<license key> \
  -v /sys/fs/cgroup:/sys/fs/cgroup:ro \
  -v /var/run/docker.sock:/var/run/docker.sock \
  mbentley/newrelic-sysmond`
```
