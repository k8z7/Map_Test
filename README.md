# Map_Test

Map_Test, FrameLayout과 TextView로 구글맵 흉내/[Android]
/ 2016.09.27. 최초 작성

도움말 페이지를 이미지로 꾸미다 보니 이런 생각이 들었다.

페이지 그림 하나를 두고 가전제품 사용설명서처럼 만들면 보기에 편하겠지?

구글맵 대충 보니 복잡하다.

1. 구상 및 작업 개요

일단 FrameLayout 안에 각 match_parent 사이즈로 먼저 ImageView를 넣고 그 아래 LinearLayout을 넣으면 이미지 위에 LinearLayout이 덮인다.

투명하게 넣으면 확인이 어려우므로 "#1100ff00" 정도로 가볍게 칠해준다.

위 vertical 리니어(편의상 '루트') 안에 공간배치를 위해 필요한 TextView, horizontal 리니어 등을 입맛대로 사용할 것이다.

루트 안에 빈줄 용도의 TextView 하나를 먼저 만든다.

        <TextView android:layout_width="match_parent" android:layout_height="50dp"/>

결과 화면을 보면서 위 높이는 조정하면 된다.

그 다음으로 horizontal 리니어(배경과 구분되게 "#ffffff"), 그 리니어 안에 빈칸 용도의 TextView 하나를 만든다.

            <TextView android:layout_width="120dp" android:layout_height="match_parent"/>

결과 화면을 보면서 위 폭은 조정하면 된다.

그에 이어서 번호를 붙일 이미지 폭에 따라 순번대로 layout_width 및 textSize 조절하여 TextView를 필요한 만큼 만들면 된다.

                android:onClick="hit"

위와 같이 텍스트뷰에 클릭 이벤트 핸들러를 달아서 필요한 작업을 처리하면 될 것이다.

2. 작업 중인 디자인

<그림 : Map_Test.png>

3. 소스

생략
