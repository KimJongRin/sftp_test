from os import lseek
import paramiko
import time 
import datetime

hostID="ip addres"
Hostport ="port"
name="name"
PassWD="pw"

try : 
    dt_now = datetime.datetime.now()
    ssh=paramiko.SSHClient()
    ssh.set_missing_host_key_policy(paramiko.AutoAddPolicy)
    ssh.connect(hostID,port=Hostport,username=name,password=PassWD)
    stdin,stdout,stderr =ssh.exec_command("mkdir testDir")
    sftp = ssh.open_sftp()
    sftp.put("client_DIR","host_DIR"+str(dt_now))
    print("done")
    time.sleep(1)
    ssh.close()
except Exception as err : 
    print("fail")
    print(err)
