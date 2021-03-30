# 4. Docker Life cycle ���ؿ� ��ɾ� �ǽ�  

<br/>

## 4.1 Docker Life cycle �����ϱ�
<img src="./image_path/dockerLifeCycle.png" width="600px" height="300px" title="Docker Life Cycle" alt="dockerLifeCycle"></img>  


<br/><br/>

## 4.2 Docker Life cycle ��ɾ� �ǽ�  

<b>4.2.1 Docker �̹��� �ٿ�ε�� ����</b>  
```
$ sudo docker pull consol/tomcat-7.0
Using default tag: latest   
...
consol/tomcat-7.0:latest
docker.io/consol/tomcat-7.0:latest

$ sudo docker rmi consol/tomcat-7.0
```

<br/>

<b>4.2.2 Tomcat �����̳� ���� �� ����</b>  
```
$ sudo docker run -d --name <��������� Container Name> tomcat
```
run ����� create�� start�� ���ԵǾ� �ִ�. ���� ������ ���ÿ� ������ �Ϸ�ȴ�.

<br/>


<b>4.2.3 �������� �����̳� Ȯ��</b>  
```
$ sudo docker ps

CONTAINER ID   IMAGE     COMMAND             CREATED           STATUS          PORTS      NAMES
e9ef7e6c9732   tomcat "catalina.sh run"   17 seconds ago    Up 11 seconds     8080/tcp     tmc
```

<br/>


<b>4.2.4 ��� �����̳� Ȯ��</b>  
```
$ sudo docker ps -a
```

<br/>


<b>4.2.5 �����̳� ����</b>  
```
$ sudo docker stop <Container ID>
```

<br/>


<b>4.2.6 �����̳� ����</b>  
```
$ sudo docker rm <Container ID>
```

<br/>

�̹� �����̳ʿ� �ö� �ִ� �̹����� �����ϰ� �ʹٸ� �����̳ʸ� ���� �����ϰ� �̹����� �����ؾ� �Ѵ�.
