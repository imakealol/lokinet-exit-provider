# lokinet exit provider 

a (toy) vpn provider app server that takes ~~loki~~ oxen as payment.

## requirements

building:

* cli wallet rpc
* postgresql
* python3
* python3-flask
* python3-psycopg2
* python3-requests
* python3-kubernetes
* [pyoxenmq](https://github.com/oxen-io/oxen-pylokimq)

running:

* docker
* docker-compose

## usage

to start a new exit:

    $ docker-compose up -d

get the `.loki` address:

    $ docker-compose exec lokinet cat /data/lokinet-addr.txt

to update the exit image:

    $ docker-compose down
    $ docker-compose pull lokinet
    $ docker-compose up -d
