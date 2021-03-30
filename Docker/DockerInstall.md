# 2. Docker ��ġ�ϱ� with AWS  
<br/>

Ŭ���� ȯ���� �ƴ� On-Premise ȯ�濡�� ��ġ�Ϸ��� ������ ��η� ��ġ�ϸ� �ȴ�.  

Virtual Box�� ��ġ�ϰ� ������ ������ [�ٿ�ε�](https://drive.google.com/file/d/1JMs6Iw1_Ke7lz4g5tNqNE6ybA57CPVsD/view) �޴´�.  

<details>
<summary>Virtual Box (Click!)</summary>
    </br>
    <span>Windows��� Windows Host Version�� </span>
    <a markdown="1" href="https://www.virtualbox.org/wiki/Downloads">�ٿ�ε�</a>
    <span> �޴´�.</span>
</details>

</br>

> �ּ� �ʿ� ���  
> CPU 4�� �̻�, RAM 8GB �̻�
> - ID:PW// server1 : test1234
> - ������ ��ȯ: sudo -i  

</br></br></br>

### 2.1 AWS ȯ�濡�� Docker ��ġ�ϱ�

1. EC2 �ν��Ͻ� ����  
    
    <b>1-1 �ܰ� 1: Amazon Machine Image(AMI) ����</b>  
    <img src="./image_path/aws_docker1.png" width="600px" height="300px" title="aws_docker1" alt="aws_docker1"></img>
    - <b>Amazon Linux 2 AMI</b> ����  
    </br>

    <b>1-2 �ܰ� 2: �ν��Ͻ� ���� ����</b>  
    <img src="./image_path/aws_docker2.png" width="600px" height="300px" title="aws_docker2" alt="aws_docker2"></img>
    - VM���� ������ ���� ����� <b>t2.large</b> �� ����  
    </br>  

    <b>1-3 �ܰ� 3: �ν��Ͻ� ���� ���� ����</b>    
    <img src="./image_path/aws_docker3.png" width="600px" height="300px" title="aws_docker3" alt="aws_docker3"></img>  
    - �ۺ� IP �ڵ� �Ҵ� <b>Ȱ��ȭ</b> ����
    </br>  
 
    <b>1-4 �ܰ� 4: ���丮�� �߰�</b>  
    <img src="./image_path/aws_docker4.png" width="600px" height="300px" title="aws_docker4" alt="aws_docker4"></img>  
    - ���丮���� Default ������ ����
    - ����: �±� �߰� Ŭ��  
    </br>  

    <b>1-5 �ܰ� 5: �±� �߰� </b>  
    <img src="./image_path/aws_docker5.png" width="600px" height="300px" title="aws_docker5" alt="aws_docker5"></img>  
    - Key : Name  
    - Value : Docker_Server (���ϴ´�� ���� ����) 
    - ����: ���� �׷� ���� Ŭ��  
    </br>

    <b>1-6 �ܰ� 6: ���� �׷� ����</b>  
    <img src="./image_path/aws_docker6.png" width="600px" height="300px" title="aws_docker6" alt="aws_docker6"></img>  
    - �� ���� �׷� ����
    - ���� �׷� �̸� : <b>DOCKER_SG</b> (���ϴ´�� ���� ����)  
    - ���� �� ���� Ŭ��  
    </br>  

    <b>1-7 �ܰ� 7: �ν��Ͻ� ���� ����</b>  
    <img src="./image_path/aws_docker7.png" width="600px" height="300px" title="aws_docker7" alt="aws_docker7"></img>  
    - �����ϱ� Ŭ��  
    - <b>.pem key�� ���ٸ� ���ο� pem key ����</b>  
    </br>     

---

</br>
 
2. EC2 �ν��Ͻ� ����  
    
    <b>2-1 EC2 �ν��Ͻ� ���� Ȯ�� </b>  
    <img src="./image_path/aws_docker9.png" width="600px" height="300px" title="aws_docker9" alt="aws_docker9"></img>  
    - �ν��Ͻ� ����, ���� �˻簡 ������ ���� ������� Ȯ��  
    - �׷��� �ʴٸ� ���� �� ��ٸ���  
    </br>  

    <b>2-2 EC2 �ν��Ͻ� ����(1)</b>  
    <img src="./image_path/aws_docker10.png" width="600px" height="300px" title="aws_docker10" alt="aws_docker10"></img>  
    - ��Ŭ�� �� <b>����</b> Ŭ��
    </br>  

    <b>2-3 EC2 �ν��Ͻ� ����(2)</b>  
    <img src="./image_path/aws_docker11.png" width="600px" height="300px" title="aws_docker11" alt="aws_docker11"></img>  
    </br>  

    <b>2-4 uname -a ��ɾ� Ȯ��</b>  
    <img src="./image_path/aws_docker12.png" width="600px" height="100px" title="aws_docker12" alt="aws_docker12"></img>
     ```
    $ uname -a
    �� ��ɾ�� �ùٸ� �ּ����� Ȯ���Ѵ�.
    ```
    </br>

---

</br>

3. Docker ȯ�� ����  

    <b>3-1 Docker ��ġ�ϱ�</b>  
    ```
    $ sudo yum -y upgrade
    $ sudo yum -y install docker
    $ sudo docker -v
    Docker version 19.03.13-ce, build 4484c46
    ```
    <img src="./image_path/aws_docker13.png" width="600px" height="100px" title="aws_docker13" alt="aws_docker13"></img>  
    Docker�� ���������� ��ġ�Ǿ����� Ȯ���� �� �ִ�.  

    </br>

    <b>3-2 Docker �����ϱ�</b>  
    ```
    $ sudo service docker start
    ```

    </br>

    <b>3-3 �׷쿡 ����� �߰�</b>  
    ```
    $ sudo usermod -aG docker ec2-user
    ```

    </br>

    <b>3-4 Docker-compose ��ġ</b>  
    ```
    $ sudo curl -L https://github.com/docker/compose/releases/download/1.25.0-rc2/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
    ```
    
    </br>

    <b>Docker-compose�� ����?</b>  
    
    ���� �Ȱ��� ������ �ϴ� ���� ���� �����̳ʸ� �����Ѵٸ� ���� ������ ��ɾ �ݺ��ؼ� �Է��ؾ� �Ѵ�.  
    ������ docker compose�� �̿��ϸ� ��ɾ� �� ������ �����̳� ������ ����������.  
    ���� docker compose�� docker-compose.yaml ���Ϸ� �����Ѵ�.  

    </br>

    > <b>Docker Compose & Kubernetes</b></br>  
     Docker compose�� ����� ���� Kubernetes�� ����� ������ ȥ�������� �� �ִ�.  
    <b>.yaml ���Ͽ� ���ǵ� �������� �����̳ʸ� �����</b>�� ����� �������� ���� �����̴�.  
    
    ���� ���̴�..  
    <b>1. Kubernetes</b>  
    - �����Ƽ�� Ŭ������ ������ �����̳ʸ� �����ϰ� �����ϴ� �����̳� ���� ����  
    - yaml ���Ͽ� ���ǵ� ������ �������� �����Ƽ�� Ŭ������ ������ �����Ƽ�� ������Ʈ�� ����� ��Ʈ�ѷ��� �����.  

    <b>2. Docker Compose</b>  
    - yaml ���Ͽ� ���ǵ� ������ �������� Host ��ǻ�� ���� �����̳ʸ� �����.  

    </br>

    <b>3-5 ������� �߰��ϱ�</b>  
    ```
    $ sudo chmod +x /usr/local/bin/docker-compose
    ```
    ��ġ �Ŀ� chmod ��ɾ ����Ͽ� ���丮�� excute ������ �߰��Ѵ�.  

    </br>

    <b>3-6 ��ġ Ȯ���ϱ�</b>  
    ```
    $ sudo docker-compose -v
    docker-compose version 1.25.0-rc2, build 661ac20e
    ```
    


</br>


---


4. Docker ��ɾ� Ȯ��


</br></br></br>

## References

[������](https://www.youtube.com/watch?v=OrK3Z1CimuU&list=PLnIaYcDMsSczk-byS2iCDmQCfVU_KHWDk&index=4&ab_channel=%EC%9E%AC%EC%A6%90%EB%B3%B4%ED%94%84)  

