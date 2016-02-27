## Project page test

This is a test for setting up project pages with custom domain names.

### Setting DNS records
The A records tell clients to go to the GitHub page servers and find which project is hosting the desired page. The host project needs to have a CNAME file that lets the GitHub page servers know that it is hosting the custom domain. Also, the CNAME record below tells the DNS provider to redirect www.<site-name>.com to <site-name>.com. TTL corresponds to a timeout.

-----------------------------------------
| Host | Type  | Address/Value   | TTL  |
-----------------------------------------
|      |   A   | 192.30.252.153  | 1800 |
|      |   A   | 192.30.252.154  | 1800 |
| www  | CNAME | <site-name>.com | 1800 |
-----------------------------------------
