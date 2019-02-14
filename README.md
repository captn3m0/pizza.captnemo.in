# pizza.captnemo.in

A simple demo nginx application for testing Certificate Authentication.

## Local Testing

1. Import the `user.pfx` file in your browser.
2. Run `docker run -ip 8443:443 capt3m0/pizza`
3. Open `https://localhost:8443` in your browser and ignore the SSL warning.

The name is [inspired from the Cloudflare TLS Client](https://support.cloudflare.com/hc/en-us/articles/115000088491-Cloudflare-TLS-Client-Auth) Auth testing website, https://auth.pizza
