# Sample static site for Piku

This is a simple static website app for Piku that demonstrates a gh-pages style `git push` workflow for deploying static sites to your Piku server.

To publish this app your Piku server, clone this repository and run the following commands:

```bash
git remote add piku piku@your_server:staticsite
git push piku master
```

Then you can set up an SSL cert and connect a domain by setting config variables like this:

```bash
ssh piku@your_server config:set staticsite NGINX_SERVER_NAME=your_site_domain_name NGINX_HTTPS_ONLY=1
```

Or if you have the `piku` command line client:

```bash
piku config:set NGINX_SERVER_NAME=your_site_domain_name NGINX_HTTPS_ONLY=1
```

Then visit the site `your_site_domain_name` and you will see a simple static site.
