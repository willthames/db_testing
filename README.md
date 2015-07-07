# Hypothesis

Postgresql network transfers are no faster on 9.3 or 9.4 than 9.2

# Assumptions

Postgresql is as fast or faster than Mysql on the same host
Mysql performance is better over the network

# Method

## Hosts
For each DB instance, install database and dependencies for local testing
to validate assumption that local performance is comparable.

Test performance over network. Compare all three databases from both clients.

### Databases
Mysql 5.1 DB (CentOS 6) (m4.large) ami-b3523089
Postgresql 9.2 DB (CentOS 7) (m4.large) ami-bd523087
Postgresql 9.4 DB (CentOS 7) (m4.large) ami-bd523087

### Clients 
Client host with Postgresql 9.2 libraries (t2.small) ami-bd523087
Client host with Postgresql 9.4 libraries (t2.small) ami-bd523087
