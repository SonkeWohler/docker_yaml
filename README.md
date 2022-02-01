# A Docker Hello World

This is a simple `docker-compose.yaml` that ties up a little project I used to
get to know some technologies that are still new to me.

## Angular

You can find the code for that [here](https://github.com/SonkeWohler/frontend).
It simply fetches a message via a HTTP request and displays it.

## Python Flask

You can find this code [here](https://github.com/SonkeWohler/backend).  It
sends a `Hello World` message on request.

## Docker

I wrapped both the above applications in docker using
[nginx](https://hub.docker.com/_/nginx/) to run the Angular application that
was built in
[node](https://hub.docker.com/_/node?tab=description&amp%3Bpage=1&amp%3Bname=alpine)
and using the basic [python image ](https://hub.docker.com/_/python/) for the
flask side.  On that last one, I haven't looked too much into it, but it
appears I shouldn't use python and alpine together in docker, [according to
some](https://pythonspeed.com/articles/alpine-docker-python/).

## Final Notes

To run simply use `docker-compose up`, in whatever tool you use to manage docker.

There is also an [alternative
implementation](https://github.com/SonkeWohler/docker_parent) of this using git
submodules and bash scripts that I really shouldn't have spent any time on, but
it was fun nonetheless.
