Creating a Traefik Stack is Easy

Pull the Repo from my Git
-------------------------
## The Following must be changed 

      - CLOUDFLARE_EMAIL=Email from Cloudflare 
      - CLOUDFLARE_DNS_API_TOKEN=DNS Token

      - "traefik.http.routers.traefik.rule=Host(`YOUR_OWN_DOMAIN`)"
      - "traefik.http.middlewares.authtraefik.basicauth.users=Artoria:$$apr1$$0a81n459$$nTRBfyWQjUaHWZujOmf3x/" password is encrypted with htpasswd use only if needed 

---------------
Do the Same in the WhoamI Container except the cloudflare data 

Dont for get to create a Network for Traefik and define it in the compose file 

And then it Should be a Simple

docker-compose up -d 

und Traefik should be Reachable on your Domain



        