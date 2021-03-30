# 2. Install Docker  
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
    1-1 �ܰ� 1: Amazon Machine Image(AMI) ����  
    <img src="./image_path/aws_docker1.png" width="600px" height="300px" title="aws_docker1" alt="aws_docker1"></img>
    - <b>Amazon Linux 2 AMI</b> ����  
    </br>

    1-2 �ܰ� 2: �ν��Ͻ� ���� ����  
    <img src="./image_path/aws_docker2.png" width="600px" height="300px" title="aws_docker2" alt="aws_docker2"></img>
    - VM���� ������ ���� ����� <b>t2.large</b> �� ����  
    </br>  

    1-3 �ܰ� 3: �ν��Ͻ� ���� ���� ����    
    <img src="./image_path/aws_docker3.png" width="600px" height="300px" title="aws_docker3" alt="aws_docker3"></img>  
    - �ۺ� IP �ڵ� �Ҵ� <b>Ȱ��ȭ</b> ����
    </br>  
 
    1-4 �ܰ� 4: ���丮�� �߰�  
    <img src="./image_path/aws_docker4.png" width="600px" height="300px" title="aws_docker4" alt="aws_docker4"></img>  
    - ���丮���� Default ������ ����
    - ����: �±� �߰� Ŭ��
    </br>  

    1-5 �ܰ� 5: �±� �߰�  
    <img src="./image_path/aws_docker5.png" width="600px" height="300px" title="aws_docker5" alt="aws_docker5"></img>
    - Key : Name  
    - Value : Docker_Server (���ϴ´�� ���� ����) 
    - ����: ���� �׷� ���� Ŭ��  
    </br>

    1-6 �ܰ� 6: ���� �׷� ����  
    <img src="./image_path/aws_docker6.png" width="600px" height="300px" title="aws_docker6" alt="aws_docker6"></img>  
    - �� ���� �׷� ����
    - ���� �׷� �̸� : <b>DOCKER_SG</b> (���ϴ´�� ���� ����)  
    - ���� �� ���� Ŭ��  
    </br>  

    1-7 �ܰ� 7: �ν��Ͻ� ���� ����  
    <img src="./image_path/aws_docker7.png" width="600px" height="300px" title="aws_docker7" alt="aws_docker7"></img>  
    - �����ϱ� Ŭ��  
    </br>  

2. EC2 �ν��Ͻ� ����


3. Docker ȯ�� ����


4. Docker ��ɾ� Ȯ��


</br></br></br>

## References

[������](https://www.youtube.com/watch?v=OrK3Z1CimuU&list=PLnIaYcDMsSczk-byS2iCDmQCfVU_KHWDk&index=4&ab_channel=%EC%9E%AC%EC%A6%90%EB%B3%B4%ED%94%84)  

