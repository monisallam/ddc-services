# ddc-services
This repo contains sample tools and mechanisms for deploying load balancing and service discovery for services deployed using 'docker run' as well as synchronizing time between UCP and DTR using bash and crontab, in an attempt to maintain quorum of the raft protocol


These are meant to be used with DDC 2.X, but could be used with any version of DDC to accomplish the same functionality

How to use:

Set up a cronjob on every node that you want to be time synced, and point that job at the update-time script.

Example:

crontab -e

and for a cronjob to run every 5 minutes...

*/5 * * * * /path/to/update-time.sh

crontab -l

should list your cronjob
