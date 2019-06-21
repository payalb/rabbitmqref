rabbitmqctl stop_app
Save erlang cookie in C:/Users/ Administrator and C:/windows


Restart rabbitmq service in services.bat 

rabbitmqctl start_app

configure hosts at C:\Windows\System32\drivers\etc\hosts and make an entry for masternode.

# rabbitmqctl forget_cluster_node rabbit@rabbit1

rabbitmqctl stop_app
rabbitmqctl join_cluster rabbit@masternode --ram //to join it as a ram node
rabbitmqctl start_app

rabbitmqctl change_cluster_node_type ram//to change node type
