# Gveluk_platform
Gveluk Platform repository

HomeTask2:

«адание:
–азберитесь почему все pod в namespace kube-system восстановились после удалени€.

ќтвет:

ѕод kube-proxy управл€етс€ контроллером DaemonSet:
Controlled By:  DaemonSet/kube-proxy
ј этот контроллер гарантирует, что все (или некоторые) узлы запускают копию модул€.

ѕод coredns управл€етс€ контроллером ReplicaSet:
Controlled By:  ReplicaSet/coredns-74ff55c5b
÷елью этого контроллера €вл€етс€ поддержание стабильного набора реплик, работающих в любой момент времени.


ѕод etcd-minikube, kube-apiserver-minikube, kube-controller-manager-minikube и kube-scheduler-minikube управл€етс€ узлом Node:
Controlled By:  Node/minikube
ј на каждом узле гарантируетс€ поддержание необходимого на бора подов. 
” нас узел один (совмещен с мастер-узлом) - а что будет при разделении, непон€тно.


HomeTask3:
«адание: почему обновление ReplicaSet не повлекло обновление запущенных pod?
ќтвет: ReplicaSet не провер€ет соответствие запущенных Podов шаблону, а следит только за тем, чтобы число подов соответствовало заданному.

¬ыполнены основное и все дополнительные задани€.

