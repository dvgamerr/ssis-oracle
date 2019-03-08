# SSIS with Oracle Instant Client 11.2

## Installation
1. Download [ODAC112040Xcopy_64bit.zip](https://drive.google.com/open?id=1tq3xHmbSc_I_z88Hyp5_xu1BqKHW_C39) to your computer.
2. Extract file and Install with command with administrator.
```batch
install.bat all c:\oracle odac
```
3. Download [instantclient-basic-windows.x64-11.2.0.4.0.zip](https://drive.google.com/open?id=1XiyT2Ro8jfv_RdmKrMvOBVQSd7cbVhGA) and extract to `c:\oracle\instantclient_11_2`
4. Set environment name
```env
PATH=C:\oracle\instantclient_11_2
TNS_ADMIN=C:\oracle\network\admin\sample
```
5. editor `tnsname.ora`
```text
# <alias> = Name to use in the connection string Data Source
# <hostname> = name or IP of the database server machine
# <port> = database server machine port to use
# <sid> = name of the database service on the server

<alias> = 
  (DESCRIPTION = 
    (ADDRESS = (PROTOCOL = TCP)(HOST = <hostname>)(PORT = <port>))
    (CONNECT_DATA =
      (SERVER = <hostname or IP>)
      (SID = <sid>)
    )
  )

```
