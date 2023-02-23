# Postgres Playground
This is docker-compose I used to set up the Postgres playground I was using in class.

I ran it in 3 terminals.


## Start the Server
In terminal 1, I ran the following:

```
docker-compose up pgserver
```
This starts up the centralized Postgres server.  This runs on a virtual subnet with the hostname pgserver with a default admin account set up: username `postgres`; password `secret`.

## Start the first client
In terminal 2, I ran the following:

```
docker-compose run pgclient
```
This runs `psql`, the postgres command-line client and connects to the `pgserver` host.

When prompted for the password enter `secret`

## Start the second client
In terminal 3, repeat the steps you performed in terminal 2.

You should be able to reproduce the exercises we did in class.


# Caveat
This is just a demo environment. The database server running in the `pgserver` container is storing to the container's local disk. When you shut down your container, this will be lost.
