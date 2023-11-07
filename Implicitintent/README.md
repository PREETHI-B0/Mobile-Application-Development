## Ex.No:3 Develop program to create a text field and a button “Navigate”. When you enter “www.google.com” and press navigate button it should open google page using Implicit Intents.
## AIM:
To create a navigate button using Implicit Intent to display the google page using Android Studio.

## EQUIPMENTS REQUIRED:
Latest Version Android Studio

## ALGORITHM:
Step1:Open Android Studio and create a new project.
Step2:In the activity_main.xml file, design the layout with a TextInputEditText element for the text field and a Button element for the "Navigate" button.
Step3:In the MainActivity.java file, retrieve references to the text field and the button using their IDs.
Step4:Set an OnClickListener for the button.
Step5:Inside the OnClickListener, retrieve the text entered in the text field using the getText() method.
Step6:Create an Intent object to open a web page with the URL obtained from the text field.
Step7:Set the action of the intent to Intent.ACTION_VIEW to indicate that the intent is used for viewing something.
Step8:Set the data of the intent to the URL obtained from the text field using the Uri.parse() method.
Step9:Set the type of the intent to "text/html" or "text/plain" to specify the type of data being viewed.
Step10:Use the startActivity() method with the intent to start the activity that can handle the implicit intent.
Step11:Run the application on an Android device or emulator to see the desired functionality.
## PROGRAM:
/*
Program to print the text “Implicitintent”.
Developed by: PREETHI.B
Registeration Number : 212221220040
*/
## activity_main.xml:
~~~
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">

<TextView
    android:id="@+id/textView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginStart="4dp"
    android:layout_marginTop="52dp"
    android:text="@string/enter_an_url"
    android:textSize="26sp"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent"
    tools:ignore="ExtraText" />

<EditText
    android:id="@+id/E1"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginTop="120dp"
    android:ems="10"
    android:inputType="textPersonName"
    android:text=""
    android:textColor="#2196F3"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.791"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

<Button
    android:id="@+id/button"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginBottom="484dp"
    android:text="Jump Into"
    app:backgroundTint="#4CAF50"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintHorizontal_bias="0.462"
    app:layout_constraintStart_toStartOf="parent" />


</androidx.constraintlayout.widget.ConstraintLayout>
~~~
## MainActivity.java:
~~~
package com.example.intent_implementation;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

public class MainActivity extends AppCompatActivity {
Button button;
EditText e1;

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    button = findViewById(R.id.button);
    e1 = findViewById(R.id.E1);
    button.setOnClickListener(view -> {
        String url = e1.getText().toString();
        Intent i1 = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
        startActivity(i1);
    });
}
}
~~~
## OUTPUT:
![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/743c7ad2-f98e-45f6-93ff-b960828c8272)
![image](https://github.com/PREETHI-B0/Mobile-Application-Development/assets/136311079/37786ba3-51e0-40f1-a943-ba592700fd6f)
## RESULT:
Thus a Simple Android Application create a navigate button using Implicit Intent to display the google page using Android Studio is developed and executed successfully.
