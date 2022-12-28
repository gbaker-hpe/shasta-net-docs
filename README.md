# THIS IS AN UNOFFICIAL DRAFT

This is a working repository to develop a better method of organizing documentation for the Shasta management network and rendering it as HTML.

## Todo

- [ ] Get Hugo static site generation working
- [ ] Integrate search that support analytics
- [ ] Integrate site analytics (Google analytics?)
- [ ] Create a organized index.html page
- [ ] Implement tabbed code examples based on switch vendor
- [ ] Move embedded images into a CDN for faster git clones

## Development Notes

I use the (klakegg/hugo:0.101.0-alpine container)[https://hub.docker.com/r/klakegg/hugo] for development.  It contains a base installation of Hugo that can be used for builds, hosting a development web server, or interactively working with the Hugo CLI.

These instructions should support (or at least easily adapt to) Windows, MacOS, and Linux.  I'm currently developing on Windows using WSL 2, which should be the hardest use-case.  MacOS and Linux should just work.

### Pulling the Hugo container image (Alpine)

```
docker pull klakegg/hugo:0.101.0-alpine
```

### Building the project

(From the project top-level directory)

```
docker run --rm -it --name hugo -v $(pwd)/src:/src klakegg/hugo:0.101.0-alpine
```

### Launching the Hugo shell from the top-level project directory

(From the project top-level directory)

```
docker run --rm -it --name hugo -v $(pwd)/src:/src klakegg/hugo:0.101.0-alpine shell
```