# Gveluk_platform
Gveluk Platform repository

HomeTask2:

Задание:
Разберитесь почему все pod в namespace kube-system восстановились после удаления.

Ответ:

Под kube-proxy управляется контроллером DaemonSet:
Controlled By:  DaemonSet/kube-proxy
А этот контроллер гарантирует, что все (или некоторые) узлы запускают копию модуля.

Под coredns управляется контроллером ReplicaSet:
Controlled By:  ReplicaSet/coredns-74ff55c5b
Целью этого контроллера является поддержание стабильного набора реплик, работающих в любой момент времени.


Под etcd-minikube, kube-apiserver-minikube, kube-controller-manager-minikube и kube-scheduler-minikube управляется узлом Node:
Controlled By:  Node/minikube
А на каждом узле гарантируется поддержание необходимого на бора подов. 
У нас узел один (совмещен с мастер-узлом) - а что будет при разделении, непонятно.
