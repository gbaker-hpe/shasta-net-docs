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

### Launching the Hugo shell from the top-level project directory

```
docker pull klakegg/hugo:0.101.0-alpine
docker run --rm -it --name hugo -v $(pwd)/src:/src klakegg/hugo:0.101.0-alpine shell
```