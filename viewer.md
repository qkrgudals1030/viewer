### WinUI 3를 사용하여 간단한 사진 뷰어 만들기

### 실습 과정 

### 1단계 sdk용 도구를 설치합니다.

### 2단계 새 프로젝트 만들기

프로젝트 이름을 SimplePhotos로 지정하고, (폴더 구조가 이 자습서에서 설명하는 구조와 일치하도록) 솔루션 및 프로젝트를 같은 디렉터리에 배치를 선택 취소합니다.

### 3단계 자산 파일 복사

zip파일을 다운후 이미지폴더를 해당 프로젝트 리포지토토리에 있는 asset폴더에 자식폴더인 samples를 만들고 이미지를 붙여준다.

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/9dc9dc76-b0e5-4708-bf18-2adb0e652830)

![image](https://github.com/qkrgudals1030/viewer/assets/50895124/339c816a-5285-413f-bbfd-f4e4e44cf91f)

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
