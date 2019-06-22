:set noendofline binary

Removes the final new line when the file is saved.

systemctl enable firewalld
systemctl start firewalld
systemctl status firewalld
sudo firewall-cmd --add-port=15672/tcp --permanent
sudo firewall-cmd --add-port=5672/tcp --permanent
sudo firewall-cmd --add-port={4369/tcp,25672/tcp} --permanent
sudo firewall-cmd --reload
sudo firewall-cmd --list-all

sudo systemctl restart rabbitmq-server
sudo rabbitmqctl stop_app
sudo rabbitmqctl join_cluster rabbit@node01
sudo rabbitmqctl start_app
sudo rabbitmqctl cluster_status



sudo yum -y install epel-release

SSH into your RabbitMQ server 1. Let’s call it rabbitmqnode1.
Set hostname using following commands:
hostname rabbitmqnode1

hostname rabbitmqnode1
Edit the following file /etc/hosts and make the following entry there:
127.0.0.1 rabbitmqnode1
"Public/Private IP of your new RabbitMQ server" rabbitmqnode2


127.0.0.1 rabbitmqnode1
"Public/Private IP of your new RabbitMQ server" rabbitmqnode2
You’ve now set a hostname for your RabbitMQ server and told it which is the other node in the cluster you’re about to setup.
View the content in the Erlang cookie file which can be found at /var/lib/rabbitmq/ 


To be able to access management console from outside localhost, add this to /etc/rabbitmq/rabbitmq.config file:
[
{rabbit,
  [

   {tcp_listeners, [5672]},
   {loopback_users, []},

   {num_tcp_acceptors, 100}
   ]

   }
].

Add to ~/.bashrc
RABBITMQ_CONFIG_FILE=/etc/rabbitmq/rabbitmq.config
export RABBITMQ_CONFIG_FILE
