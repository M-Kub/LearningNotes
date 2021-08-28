# Important files and folders

## NGINX

Found in * /etc/nginx * 

- /sites-available | Here you configure the nginx settings in a file usually named after your site e.g. "myBlog". * sites-available * is also the only folder you should make changes in, never edit files in sites-enabled. When you are done editing your file e.g. * /etc/nginx/sites-available/myBlog * you save it, and then back in the terminal, create a symlink like this * sudo ln -s /etc/nginx/sites-available/myBlog /etc/nginx/sites-enabled *.

- /sites-enabled | Thats the folder where your * /sites-available/myBlog * file will show up after you symlinked it.

## Postgresql

The place for the config files varies from system to system on UbuntuServers it's usually found at * /etc/postgresql/11/main *.

- /pg_hba.conf | Here you make changes on how you authenticate if loging into postgresql via psql or tell your Django settings.py file how to access the PostgresDatabase. For password protection you should change the connection method to either * md5 * or * scram-sha-256 *.
