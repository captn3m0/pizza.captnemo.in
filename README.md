# pizza.captnemo.in

A simple demo nginx application for testing Certificate Authentication.

## Local Testing

1. Import the `user.pfx` file in your browser.
2. Run `docker run -ip 8443:443 captn3m0/pizza`
3. Open `https://localhost:8443` in your browser and ignore the SSL warning.
4. Alternatively, you can run `curl https://pizza.captnemo.in:8443/ --cert user.pem --cacert cert.pem --resolv pizza.captnemo.in:8443:127.0.0.1` locally.

## What are all the files?

-   `ca.crt` - CA Certificate used to sign the client certificates
-   `cert.pem` - Server TLS Certificate (PEM)
-   `key.pem` - Server TLS Private Key (PEM)
-   `user.pem` - Combined cert+key for the client (PEM)
-   `user.pfx` - Combined cert+key for the client, in pkcs12 format

The name is [inspired from the Cloudflare TLS Client](https://support.cloudflare.com/hc/en-us/articles/115000088491-Cloudflare-TLS-Client-Auth) Auth testing website, https://auth.pizza
