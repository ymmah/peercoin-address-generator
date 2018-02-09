# Running wallet via docker - Instructions

1. Clone this repo **locally** on **master branch** and run build instructions;
2. Clone this repo **on server** on **docker branch**;
3. Copy `/public` content from **local** to `/public` folder on **docker branch** you cloned in **server**;
4. Run: `docker build -t ppc-wallet .`;
5. Run: `docker run --name ppc-wallet-nginx --restart on-failure -p 5001:80 ppc-wallet`.

The Reverse-proxy and SSL files are located on local NGINX (outside of docker). They can be found at: `/etc/nginx/sites-available/default`.

SSL is generated by Let's Encrypt via certbot.

The URLs addressed are:

https://hodl.peercoin.net/
https://paperwallet.peercoin.net/