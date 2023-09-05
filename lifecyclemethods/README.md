# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
/*
Program to print the text “Hello World”.
Developed by: NIRANJANA DEVI S
Registeration Number : 212221220036
*/
## Activity_main.xml:

<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android" xmlns:app="http://schemas.android.com/apk/res-auto" xmlns:tools="http://schemas.android.com/tools" android:layout_width="match_parent" android:layout_height="match_parent" tools:context=".MainActivity">
~~~

<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:textSize="40dp"
    android:text="Hello World!"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"#
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />
~~~
## MainActivity.java:
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle; import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
~~~

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
    Toast toast = Toast.makeText(getApplicationContext(), "onCreate Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onStart() {
    super.onStart();
    Toast toast = Toast.makeText(getApplicationContext(), "onStart Called", Toast.LENGTH_LONG);
    toast.show();
}
@Override
protected void onRestart() {
    super.onRestart();
    Toast toast = Toast.makeText(getApplicationContext(), "onRestart Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onPause() {
    super.onPause();
    Toast toast = Toast.makeText(getApplicationContext(), "onPause Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onResume() {
    super.onResume();
    Toast toast = Toast.makeText(getApplicationContext(), "onResume Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onStop() {
    super.onStop();
    Toast toast = Toast.makeText(getApplicationContext(), "onStop Called", Toast.LENGTH_LONG);
    toast.show();
}
protected void onDestroy() {
    super.onDestroy();
    Toast toast = Toast.makeText(getApplicationContext(), "onDestroy Called", Toast.LENGTH_LONG);
    toast.show();
}
}
~~~


## OUTPUT
![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/57f03f0e-1794-4d20-833c-c6953420300a)
![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/6e37e41a-ab46-4c0b-be08-f3e006b2746b)
![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/bbaf4cef-1b56-489f-8561-85353de00e59)
![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/8892e508-0f07-467e-a400-2aeaa33a4a96)

![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/560d847d-c157-4fa8-8dd9-f8cdfbd06a05)
![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/dcb22d97-dea5-45b0-9ef5-e594ce686a5e)
![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/dd56a52e-7a4c-4f52-b11c-a95dc78c7bc7)

![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/da321e5c-2aa2-41b0-928f-7128831becc5)
![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/b5a7e0eb-d574-44ac-83fb-78da07acf740)



## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
