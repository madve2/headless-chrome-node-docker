# headless-chrome-node-docker

[![Docker Pulls](https://img.shields.io/docker/pulls/madve2/headless-chrome-node-docker.svg)](https://store.docker.com/community/images/madve2/headless-chrome-node-docker/tags) [![Docker Pulls](https://img.shields.io/docker/stars/madve2/headless-chrome-node-docker.svg)](https://store.docker.com/community/images/madve2/headless-chrome-node-docker/tags)

Provides a Docker image with out of the box support for the recent release of [cross-platform Headless Chrome](https://developers.google.com/web/updates/2017/04/headless-chrome) and [Node](https://nodejs.org/)(currently 12.13.1).


# Usage

```
# Dockerfile

FROM madve2/headless-chrome-node-docker:latest

CMD ["sh", "start-chrome.sh"]
```

```
# start-chrome.sh

google-chrome \
  --headless \
  --hide-scrollbars \
  --disable-gpu \
  --remote-debugging-port=9222
```

After building your docker image and running a container with it, you can connect to headless chrome inside the container on port 9222. If you're using Node.js, you can use [chrome-remote-interface](https://github.com/cyrus-and/chrome-remote-interface) module to talk to Chrome via the [Chrome Debugging Protocol](https://chromedevtools.github.io/devtools-protocol/)


# Image Size

199 MB compressed as of [last build](https://hub.docker.com/r/madve2/headless-chrome-node-docker/tags/)


# License

MIT © [Karan Thakkar](https://karanjthakkar.com), Dániel Kis-Nagy
