# SSH Tunnel Dynamic Port Forwarding Python

![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)

# New Features!

>ssh -D 1080 -N username@host


```python
def test(host, username, password, port):
  controlssh = SSHProxyControler(host, username, password, port)
  sshstatus, host, port = controlssh.start()
  print(sshstatus, host, port)
  if sshstatus:

    time.sleep(30) #Make some request right here

    controlssh.stop()
    print('SSH is Stoped')
  else:
    print('Can not connect to SSH')

test('14.177.235.133', 'admin', 'admin', 1082)

```

## Installation
```
pip3 install asyncssh
```
* [asyncssh] - Full support for SSHv2, SFTP, and SCP client and server functions


## asyncio python link
   [asyncssh]: <https://pypi.org/project/asyncssh/>

