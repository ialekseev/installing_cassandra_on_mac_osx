# Installing Cassandra on Mac OS X (via Brew)

*Install Homebrew:*
```
ruby -e "$(curl -fsSL https://raw.github.com/Homebrew/homebrew/go/install)"
```
*Install Python:*
```
brew install python
```
*Install cql:*
```
pip install cql
```
*Install Cassandra:*
```
brew install cassandra
```
*Starting/Stopping Cassandra:*
Probably it's better NOT to start Cassandra on startup (using plist file from ~/Library/LaunchAgents/). Instead we just start/stop it when it's needed:
```
launchctl load /usr/local/opt/cassandra/homebrew.mxcl.cassandra.plist
launchctl unload /usr/local/opt/cassandra/homebrew.mxcl.cassandra.plist
```

Cassandra file locations
------------------------
Properties: /usr/local/etc/cassandra  
Logs: /usr/local/var/log/cassandra  
Data: /usr/local/var/lib/cassandra/data  
Cassandra itself: /usr/local/Cellar/cassandra/{version}   
Versionless alias: /usr/local/opt/cassandra    

Connect to cassandra using cqlsh:
------------------------------------------
```
$> cqlsh
Connected to Test Cluster at 127.0.0.1:9042.
[cqlsh 5.0.1 | Cassandra 2.1.2 | CQL spec 3.2.0 | Native protocol v3]
Use HELP for help.
cqlsh>
cqlsh>
```
