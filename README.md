## Grafana dashboard for BigBlueButton

The provided `docker-compose` should work out of the box as an all in one solution.
In theory in has all the data necessary to be up and running in a matter
of minutes. Add a user to grafana and it should pick up all the data
from you BigBlueButton instance right away.

To get started make sure you have `Docker` and `docker-compose`
installed. Then rename the `bbb.env.example` file to `bbb.env` and add
ypur server details. To get the `Secret` run `bbb-conf --secret` on your
bbb server.

Additionally there is an influxdb server to monitor the server itself.

I like the influxdb dashboards slightly better for server monitoring so
I have added that as well to the `docker-compose` file. To set up a
server add a telegraf configuration, create a new bucket and install
telegraf on your server. Influxdb will give you the config file.
