#### Screen
* sudo service mongod start
* screen -S dashboard -d -m sudo sbt run -Dhttp.port=80
* screen -r <session name>
* Ctrl + a then d

#### Supervisord
* Tell Supervisor to read all of the configuration files: reread
* Add the foo program: add foo
* status
* start foo
* restart foo
* stop foo
* tail foo stderr
* tail foo stdout
* tail -f foo
* tail -f foo stderr
* help

lsof -i :port
