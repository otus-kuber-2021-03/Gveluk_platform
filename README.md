# Gveluk_platform
Gveluk Platform repository

HomeTask2:

�������:
����������� ������ ��� pod � namespace kube-system �������������� ����� ��������.

�����:

��� kube-proxy ����������� ������������ DaemonSet:
Controlled By:  DaemonSet/kube-proxy
� ���� ���������� �����������, ��� ��� (��� ���������) ���� ��������� ����� ������.

��� coredns ����������� ������������ ReplicaSet:
Controlled By:  ReplicaSet/coredns-74ff55c5b
����� ����� ����������� �������� ����������� ����������� ������ ������, ���������� � ����� ������ �������.


��� etcd-minikube, kube-apiserver-minikube, kube-controller-manager-minikube � kube-scheduler-minikube ����������� ����� Node:
Controlled By:  Node/minikube
� �� ������ ���� ������������� ����������� ������������ �� ���� �����. 
� ��� ���� ���� (�������� � ������-�����) - � ��� ����� ��� ����������, ���������.
