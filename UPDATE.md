1. create new branch on top of newest '...my-setup'
2. name this branch like the target tag with the '-my-setup' postfix
3. merge the newest tag to it `git merge #tagname#`
4. ensure that `SENTRY_EVENT_RETENTION_DAYS` is not 90 days in `.env-org`
5. compare the `docker-compose.yml` differences against the current '...my-setup' branch
   1. for new services, add 'sentry' network
   2. for new permanent volumes, ensure folder mapping is set
   3. for nginx, ensure `nginx_net` network is set
   3. for nginx, ensure `hostname` network is set
