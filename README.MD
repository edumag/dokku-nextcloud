# Run Nextcloud as a Dokku app

1. Install dokku plugins:
   - [dokku-postgres](https://github.com/dokku/dokku-postgres)
   - [dokku-require](https://github.com/crisward/dokku-require/)
2. Clone/fork this repo
3. Create `nextcloud` app
4. Set `NEXTCLOUD_ADMIN_USER` and `NEXTCLOUD_ADMIN_PASSWORD` env variables
5. Push to dokku
6. sudo mkdir /var/lib/dokku/data/storage/nextcloud # In server.
7. sudo chown dokku:dokku  /var/lib/dokku/data/storage/nextcloud/ # In server.


In summary:

```bash
dokku plugin:install https://github.com/dokku/dokku-postgres
dokku plugin:install https://github.com/crisward/dokku-require/
dokku apps:create nextcloud
dokku config:set nextcloud NEXTCLOUD_ADMIN_USER=<SET_ME> NEXTCLOUD_ADMIN_PASSWORD=<SET_ME>

git push dokku master
```
