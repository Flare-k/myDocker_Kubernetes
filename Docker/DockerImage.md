# 3. Docker���� ���ϴ� �̹��� ã��

<br/>

## 3.1 Docker Registry  

<img src="./image_path/docker_registry.png" width="600px" height="210px" title="Docker Registry" alt="docker_registry"></img>  
[�׸� ��ó]( https://github.com/dotnet-architecture/eShopModernizing/wiki/03.-Publishing-your-Windows-Container-images-into-a-Docker-Registry)

> Docker Registry���� ����ڰ� ����� �� �ֵ��� �����ͺ��̽��� ���� Image�� �������ְ� �ִ�.  
������ �̹����� ����� Push�� �� ������ Ǫ�õ� �̹����� �ٸ� ����鿡�� ���� �����ϴ�.

<b>Docker Registry : </b>������ Image ���� ������  
<b>Images : </b>Static�� ���·ν� ������ �� �� ����.  
<b>Container : </b>Image�� �����Ű�� ���� Container�� �ٲ���� �Ѵ�.  


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

## References

[������](https://www.youtube.com/watch?v=OrK3Z1CimuU&list=PLnIaYcDMsSczk-byS2iCDmQCfVU_KHWDk&index=4&ab_channel=%EC%9E%AC%EC%A6%90%EB%B3%B4%ED%94%84)  
