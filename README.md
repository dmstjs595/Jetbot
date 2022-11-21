## Jetbot!
-----------
Jetbot을 실행시켜보았다.
전원을 키면 작은 lcd화면에 ip 주소가 나타나고 (ip주소):8888을 검색창에 입력하면 주피터랩으로 접속할 수 있다. 
나의 경우에는 172.16.13.223 이었다.
Basic Motion에 있는 코드블록들을 다 실행시키고 나면 Jetbot을 움직일 수 있다. 
하지만 하드웨어상의 문제로 forward를 누르면 right로, right를 누르면 forward로, backward를 누르면 left로, left를 누르면 backward로 이동하는 오류가 생겼다.
robot.py나 motor.py 파일 등에서 speed를 조정해 수정할 수도 있지만 코드 파일들이 너무 분산되어 있었기 때문에 한계가 있었다. 
![Screenshot from 2022-11-21 20-06-07](https://user-images.githubusercontent.com/76214070/203040048-3aa3fcfe-b3f1-4b4e-b829-f07b0b575e57.png)
그래서 난 버튼 조작 인터페이스 자체를 수정하기로 했다. 
우선 각 버튼을 눌렀을 때 실제로 움직이는 방향으로 button discription을 바꿔준다. 
그러면 버튼의 위치가 바뀐다. 
이제 버튼을 우리가 친숙한 방향으로 바꾸어주면 된다.
우선 가로 방향으로는 left, stop, right 순서로 배열되어야 하기 때문에 backward, stop, forward 버튼을 배치해주고
세로 방향으로는 forward, stop, backward 순서로 배열되어야 하기 때문에 right, stop, left 버튼을 배치해준다.
이렇게 되면 버튼의 형식을 이용해 우리가 원하는 방향으로 Jetbot을 움직일 수 있다.
![Screenshot from 2022-11-21 20-02-24](https://user-images.githubusercontent.com/76214070/203038794-dc489e0b-893a-4824-af3a-4e856c4f80d1.png)
슬라이더를 이용해 Jetbot을 회전시킬 수도 있다.
각각 왼쪽, 오른쪽 바퀴를 나타내는 두 개의 슬라이더를 조절해 바퀴의 회전 정도를 조절할 수 있다.
![Screenshot from 2022-11-21 20-03-57](https://user-images.githubusercontent.com/76214070/203039954-e2bc833d-8969-4ad1-88b6-26af5cd5976f.png)
