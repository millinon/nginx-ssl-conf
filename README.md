# Nginx SSL/TLS Configuration

---

This is mostly here just so that I don't have to go hunt down the recommended Nginx configuration whenever I set up a new server. It can be cloned into the /etc/nginx/ directory.

The file `site-ssl.conf` is intended to be included in the configuration wherever a server that uses SSL is defined, such as in `/etc/nginx/sites-available/example.com`:

    server {
        ...
        include /etc/nginx/nginx-ssl-conf/site-ssl.conf;
        ...
    }

An example is present in the file itself. The paths are set up as if the certificates and keys are produced by Letsencrypt, but they can be modified for different paths.

---

## Disclaimer

I am not a security professional, so do not use this configuration in production. There may be errors in the configuration that at best prevent Nginx from starting and at worst create a vulnerability in your server.

---

## Sources

The following pages were borrowed from:

https://scotthelme.co.uk/hpkp-http-public-key-pinning/

https://gist.github.com/plentz/6737338
