### SUPERVISOR

#### supervisord
*  Starts process as its children to be able to monitor
  - No PID file monitoring as monitor
* Auto-restart in case of a crash
* Process groups let supervisor start process in order

#### supervisord
* responsible for starting child programs at its own invocation
* server process uses a configuration file
* /etc/supervisord.conf
* keep this file secure via proper filesystem permissions

#### supervisorctl
* a user can connect to different supervisord processes
* get status on the subprocesses controlled by
* stop and start subprocesses of
* and get lists of running processes of a supervisord.

#### installation https://gist.github.com/fadhlirahim/78fefdfdf4b96d9ea9b8
* pip install supervisor
* echo_supervisord_conf > /etc/supervisord.conf to echo sample conf
* sudo vi /Library/LaunchDaemons/com.agendaless.supervisord.plist
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
    <key>KeepAlive</key>
    <dict>
        <key>SuccessfulExit</key>
        <false/>
    </dict>
    <key>Label</key>
    <string>com.agendaless.supervisord</string>
    <key>ProgramArguments</key>
    <array>
        <string>/usr/local/bin/supervisord</string>
        <string>-n</string>
        <string>-c</string>
        <string>/usr/local/share/supervisor/supervisord.conf</string>
    </array>
    <key>RunAtLoad</key>
    <true/>
</dict>
</plist>

#### running
* [program:foo]
command=/bin/cat ;sample program
* supervisord ;to run

#### configuration


### Features
#### Simple

Supervisor is configured through a simple INI-style config file that’s easy to learn. It provides many per-process options that make your life easier like restarting failed processes and automatic log rotation.
Centralized

Supervisor provides you with one place to start, stop, and monitor your processes. Processes can be controlled individually or in groups. You can configure Supervisor to provide a local or remote command line and web interface.
#### Efficient

Supervisor starts its subprocesses via fork/exec and subprocesses don’t daemonize. The operating system signals Supervisor immediately when a process terminates, unlike some solutions that rely on troublesome PID files and periodic polling to restart failed processes.
#### Extensible

Supervisor has a simple event notification protocol that programs written in any language can use to monitor it, and an XML-RPC interface for control. It is also built with extension points that can be leveraged by Python developers.
#### Compatible

Supervisor works on just about everything except for Windows. It is tested and supported on Linux, Mac OS X, Solaris, and FreeBSD. It is written entirely in Python, so installation does not require a C compiler.
#### Proven

While Supervisor is very actively developed today, it is not new software. Supervisor has been around for years and is already in use on many servers.
