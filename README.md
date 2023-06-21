# dex_caddy_docker_compose
This is a template for setting up Dex in a VM using Docker compose. In this setup Caddy acts as reverse proxy, Caddy is preferred as it provides auto SSL.


Steps:
1. Spin up a VM with the following ports exposed 22(ssh), 80(http) and 443(https).
2. Install docker and docker-compose
3. Clone this repository in your VM.
4. Replace `<YOUR_DOMAIN_HERE>` with your domain name in the `Caddyfile` and `dex-config.yaml`.
5. Setup DNS for your domain to point to the VM address.
6. Once the DNS is propogated run docker-compose up.
7. Caddy will take few mins to complete the SSL setup.


For more information on configuring dex refer the example config from [here](https://github.com/dexidp/dex/blob/master/examples/config-dev.yaml).
