How to Run AMQP Client :
------------------------

Install QPID Proton for Python

#pip install python-qpid-proton

Run AMQP Client:
----------------

python amqpClient.py -c -i S1 -d -p amqp.properties -f test1.log

## Where "test1.log" is the log file
## Where s1 is the clientId
## Where "-p" is to define the property file
## Where amqp.properties is the property file 
## -c is to show it as a cluster
## -d is to show it as a durable client

Properties in amqp.properties file:
----------------------------------

[DETAILS]
UserName=jmsclient%40csp	
Password=jmsclient
TopicName=topic/CNAMessages
#TopicName=topic/CNATopic
#QueueName=queue/CNAQueue

[CONNECTION]
Port=5672
IpAddr1=1.1.1.1
IpAddr2=2.2.2.2
IpAddr3=3.3.3.3


Where UserName mentioned here should be defined in VSD with enterprise in the same format i.e., jmsclient%40csp. Here jmsclient is the username and csp is the enterprise. 
Password should match the password created for the user in VSD.
TopicName can be either CNAMessages or CNATopic or CNAQueue as shown in property file
Port should be 5672 as AMQP client uses 5672 port to communicate with VSD
IpAddr1, IpAddr2, IpAddr3 are the cluster node IP Addresses.



