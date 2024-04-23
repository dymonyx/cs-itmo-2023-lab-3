# Лабораторная работа 3
## Установка трёх виртуальных машин с GUI ubuntu
> [!NOTE]
> Предварительно был скачан virtualbox с помощью sudo apt install virtualbox

На основе iso образа linux ibintu были созданы три виртуальные машины:
- virtual_machine_A (машина А)
- virtual_machine_B (машина Б)
- virtual_machine_C (машина В)
![создание виртуальных машин](/Report/Screenshot-3.png)
На каждой машине была установлена ubuntu:
![установка ubuntu на каждую машину](/Report/Screenshot-2.png)
## Подключение всех машин к общей сети NAT
>**Note**
>Network Address Translation (NAT) is the simplest way of accessing an external network from a virtual machine. Usually, it does not require any configuration on the host network and guest system. For this reason, it is the default networking mode in Oracle VM VirtualBox.
>A virtual machine with NAT enabled acts much like a real computer that connects to the Internet through a router. The router, in this case, is the Oracle VM VirtualBox networking engine, which maps traffic from and to the virtual machine transparently. In Oracle VM VirtualBox this router is placed between each virtual machine and the host.

С помощью сети NAT были соединены все машины, а также был получен доступ в интернет. Сеть была создана в настройках virtualbox.
![NAT virtualbox](/Report/Screenshot-10.png)
![подключение всех машин к сети nat](/Report/Screenshot.png)
## Проверка подключения машины А к интернету
![доступ машины А к интернету](/Report/Screenshot-5.png)
## Проверка подключения машины А к машине В

ip address машины B - 10.0.2.9 был присвоен автоматически.
(его видно при вызове ip a)

![доступ машины А к машине В](/Report/Screenshot-1.png)
## Проверка подключения машины А к машине C

ip address машины С - 10.0.2.6 был присвоен автоматически.

![доступ машины А к машине С](/Report/Screenshot-4.png)
## Запрет доступа машины В к машине С

Запрет был реализован при помощи фаервола iptables и общего сетевого интерфейса enp0s3.

![запрет доступа машины В к машине С](/Report/Screenshot-6.png)
## Терминалы всех машин на одном скриншоте
![терминалы всех машин 1](/Report/Screenshot-7.png)
## Скриншот со всеми установлеными связями

- Машина А, ip address - 10.0.2.15
- Машина B (Б), ip address - 10.0.2.9
- Машина С (В), ip address - 10.0.2.6
![терминалы всех машин 2](/Report/Screenshot-8.png)
## Сохранение конфигурации iptables
![сохранение iptables](/Report/Screenshot-9.png)
