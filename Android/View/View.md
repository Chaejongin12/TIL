# View, 위젯의 종류와 속성
#### 뷰의 종류의 속성을 알아보겠습니다.

<br>
<br>
<br>

## 1. TextView
#### 텍스트를 표시하는 위젯 중 가장 기본적인 View이다.
<br>

#### 속성
#### text - 텍스트를 정한다.
#### textSize - 텍스트의 크기를 정한다.
#### textStyle - 텍스트의 스타일을 정한다.
#### textColor - 텍스트의 색깔을 정한다.

<br>
<br>

## 2. ImageView
#### 지정한 이미지를 보여준다. 이미지를 넣지 않고 색깔만 지정하여 색으로만 칠해서 보여줄 수 있다.
<br>

#### 속성
#### background - 이미지 뷰의 배경색을 정한다.
#### src - 선택한 이미지를 뷰에 담는다.

<br>
<br>

## 3. ScrollView
#### 뷰크기를 넘어가면 드래그하여 볼 수 있는 위젯이다.

<br>

#### 속성
#### horizontal - 뷰안의 요소를 수평으로 배치한다.
#### vertical - 뷰안의 요소를 수직으로 배치한다.

<br>
<br>
 
## 4. EditText
#### 텍스트를 입력 받을 수 있다.

<br>

#### 속성
#### gravity - 텍스트가 배치 될 위치를 정한다.
#### inputType - 입력 받는 값의 형태를 정한다. text(문자),number(숫자)등이 있다.
#### hint 입력전에 볼 수 있는 텍스트다.

<br>
<br>

## 5. Button
#### 클릭하여 입력값을 줄 수 있는 위젯이다. TextView처럼 버튼 스타일을 꾸밀 수 있다.
<br>

#### 속성
#### backgroundTint - 버튼의 색상을 정한다.
#### text - 버튼에 쓰여질 텍스트를 정한다.
#### textAllCaps - 쓰여진 텍스트를 대문자로 표시 해준다.

<br>
<br>

## 6. ImageButton
#### 버튼에 이미지를 담을 수 있다.
<br>

#### 속성
#### ProgressBar(진행바, 로딩바), SeekBar, RatingBar(평점표시), CheckBOx(선택표시), DatePicker(날짜 선택), TimePicker(시간선택) 등등이 있다.

<br>
<br>

## View의 높이와 넓이
#### View의 높이와 넓이는 다양하게 지정 할 수 있다.
#### layout_width="설정값" - 설정값에 맞게 넓이를 지정한다.
#### layout_height="설정값" - 설정값에 맞게 높이를 지정한다.

<br>

#### 설정값
#### 정수 + 단위 - 직접 숫자와 단위를 입력해 크기를 지정한다.
#### match_ parent - 뷰가 넓힐 수 있는 범위까지 최대한 채워준다.
#### wrap_parent - 뷰의 안에 담기는 것에 대해 크기를 맞춰준다.

<br>

#### **버튼에 대한 더 자세한 설명은 아래의 개발자 페이지에서 확인 할 수 있다! ✈️**
https://developer.android.com/guide/topics/ui/controls/button?hl=ko


