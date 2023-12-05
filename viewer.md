### WinUI 3를 사용하여 간단한 사진 뷰어 만들기

### 실습 과정 

### 1단계 sdk용 도구를 설치합니다.

### 2단계 새 프로젝트 만들기

프로젝트 이름을 SimplePhotos로 지정하고, (폴더 구조가 이 자습서에서 설명하는 구조와 일치하도록) 솔루션 및 프로젝트를 같은 디렉터리에 배치를 선택 취소합니다.

### 3단계 자산 파일 복사

zip파일을 다운후 이미지폴더를 해당 프로젝트 리포지토토리에 있는 asset폴더에 자식폴더인 samples를 만들고 이미지를 붙여준다.

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/9dc9dc76-b0e5-4708-bf18-2adb0e652830)

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/5c33234a-19fb-4eb4-ac1b-fd02f9e672ad)


### 4단계 GridView 컨트롤 추가

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/4d55566c-9857-4477-9d60-33752f9268ac)

메인 윈도우에 Grid 컨트롤을추가하여줍니다. 

### 5단계 ImageFileInfo 모델

1. 프로젝트 노드에서 새로운 Midl(.idl)파일을 선택후 이름을 ImageFileInfo.idl로 설정하고 추가를 클릭합니다.
  
2. ImageFileInfo.idl의 코드목록을 변경후 프로젝트를 빌드합니다. 빌드하면 일부 파일이 생성됩니다.
  
3. 생성된 파일을 생성한 프로젝트에 붙여넣어줍니다.
![image](https://github.com/qkrgudals1030/viewer/assets/50895124/afc2ebd3-4935-4a78-830f-56e776466348)


4. 붙여넣어준 파일을 프로젝트에 포함을 클릭하여 포함시켜 줍니다.

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/2764c2dc-c948-4af9-b062-56f2f09d306f)

5. pch.h 파일 끝에 다음 필수 포함을 추가합니다.

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/8b112930-e278-4e7b-9752-75ed51e710f7)

6. ImageFileInfo.h의 콘텐츠를 아래 코드 목록으로 바꿉니다.

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/754c9e77-96c4-4a38-a034-ba599fcb47aa)


7. ImageFileInfo.cpp의 콘텐츠를 아래 코드 목록으로 바꿉니다.

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/1823070e-f6ce-4208-813e-08e3f057f700)

### 6단계 이미지 컬렉션에 대한 속성 정의 및 채우기

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/8b4d8dac-528e-4d3d-bb82-5996b3b5227d)

XAML UI에서 Images 속성을 참조할 예정입니다. 이러한 이유로 Microsoft는 MainWindow 클래스에 대한 IDL 파일에서 Images 속성을 선언해야 합니다.

메서드 선언 및 정의를 MainWindow.xaml.h 및 MainWindow.xaml.cpp에 붙여넣습니다.

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/d38e50c2-6361-4fa4-b4e4-6447d03106a1)


![image](https://github.com/qkrgudals1030/viewer/assets/50895124/79b265bb-8a67-47fd-8d1b-00e8e690b858)


### 7단계: 데이터 템플릿 추가

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/f081f2f6-f198-4c5e-b78c-7deb8c38e7bd)

먼저 스케치처럼 보이는 자리 표시자 데이터 템플릿을 사용하겠습니다. 레이아웃 옵션 탐색을 완료할 때까지 사용됩니다. 그 후에는 데이터 템플릿을 업데이트하여 실제 사진을 표시할 수 있습니다.

### 결과 화면

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/bf022f0e-1b4f-465d-a9fe-09f017b01464)

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/fcff6641-02ae-4ad6-b51a-53fcbccda036)

### 작성소감

20191125 박형민 이번 팀 프로젝트를 통해 수업 시간에 교수님이 안내해 주실 때와 개별적으로 진행하는 경우의 차이를 명확히 느꼈습니다. 교수님과 함께 진행되는 수업은 따라가기가 수월했지만, 개별적으로 진행하려고 하니 어려움을 느꼈습니다. 그러나 팀 프로젝트를 수행하면서 팀원들과 함께 논의하면서 부족한 부분을 서로 보완하고, 알고 있는 내용을 공유하며 작업하니 좋은 결과를 얻을 수 있었습니다. 무작정 따라하기보다 한번 천천히 읽어보며 진행하니 조금더 수월하게 과제를 수행할 수 있었던것 같습니다. 마지막으로 과제를 완성시켜보면서 프로그래밍하는 것에 대한 자신감을 얻을 수 있었습니다. 비쥬얼 프로그래밍 화이팅!!!

20191122 김준영 과제 수행 중에는 WinUI 갤러리, 카페, 그리고 마이크로소프트의 자료를 참조하면서, 모르는 부분은 팀원들과 상호간에 물어보고 챗지피티를 활용하여 해결했습니다. 이런 협업과 의사소통을 통해 어려운 부분도 해결하고, 서로 도움을 주고 받으며 과제를 성공적으로 수행할 수 있었습니다. 앞으로는 과제를 천천히 읽어가며 해결해 나가면 할 수 있다는 자신감을 얻었습니다.





