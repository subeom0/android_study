```xml
  <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/bg"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".login">
 ```
 레이아웃에 대한 속성이다
 
 ```xml
 tools:context=".login"
 ```
 해당 xml과 연결될 코드파일을 정하는 곳이다 
 
 ```xml
android:hint="ID"
```
텍스트박스에 회색글자로 ID를 출력시킨다. 클릭하면 지울 필요없이 사라진다
입력해야할 정보를 알려줄 수 있다

```xml
android:text="login"
```
텍스트 입력

```xml
android:textSize="30dp"
```
텍스트크기 변경

```xml
android:ems="10"
```
텍스트박스의 너비 설정

```xml
android:textColor="@color/black"
```
텍스트 색 설정 
이때 color/뒤에 들어가는 색상은 app/res/values/colors.xml에서 
```xml
<color name="black">#FF000000</color>
``` 
이렇게 색상코드로 선언하고 사용해야한다.
코드표 
`https://m.blog.naver.com/hellonami/30189427178`

```xml
android:backgroundTint="@color/white"
```
버튼색 변경 
*하지만 이렇게 해결할 경우 xml로 정의한 커스텀버튼을 사용할 수 없다*

따라서 app\src\main\res\values\themes.xml에서 3번째 줄에 있는 테마를
```xml
<style name="Theme.프로젝트명" parent="Theme.AppCompat.Light">
```
로 바꾸면 된다.

Missing autofillHints 경고

```
android:autofillHints="no"
```
추가시 해결

use string resourse 경고
doe/app/src/main/res/values/strings.xml에서 
```xml
<string name="pw">password</string>
```
형식으로 선언 후 

```xml
android:hint="@string/pw"
```
