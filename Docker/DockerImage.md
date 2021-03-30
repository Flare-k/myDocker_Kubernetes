# 3. ���ϴ� Docker �̹��� ã��

<br/>

## 3.1 Docker Registry  

> Docker Registry���� ����ڰ� ����� �� �ֵ��� �����ͺ��̽��� ���� Image�� �������ְ� �ִ�.  
������ �̹����� ����� Push�� �� ������ Ǫ�õ� �̹����� �ٸ� ����鿡�� ���� �����ϴ�.

<br/>

## 3.2 Docker Public Registry �˻� �� Ȯ��
[Docker hub]([https://hub.docker.com/](https://hub.docker.com/))���� � Image���� �ִ��� Ȯ���� �� �ִ�.  

- <b>3.2.1 Docker ��ɾ�� �˻�</b>  
    tomcat image�� ã�ƺ���

    ```
    $ sudo docker search tomcat
    ```

    <br/>

- <b>3.2.2 Docker �̹��� �ٿ�ε��ϱ�</b>  

    ```
    $ sudo docker pull tomcat
    Using default tag: latest
    latest: Pulling from library/tomcat
    8bf9c589d5f9: Pull complete 
    4c70e46d8b5f: Pull complete 
    ea848ad42f0d: Pull complete 
    ...
    docker.io/library/tomcat:latest
    ```

    <br/>

- <b>3.2.3 ���� �ý��ۿ� �ִ� Docker �̹��� Ȯ���ϱ�</b>  

    ```
    $ sudo docker images
    REPOSITORY  TAG      IMAGE ID      CREATED      SIZE  
    tomcat     latest  0ce438e89a29   2 days ago    667MB
    ```

    <br/>

<br/>

[�ڷΰ���](/Docker/README.md)  

<br/>

---