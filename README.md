![Screenshot (8)](https://user-images.githubusercontent.com/80418238/110731127-bd96d600-8247-11eb-967a-87640266439e.png)
![Screenshot (8)](https://user-images.githubusercontent.com/80418238/110731203-e8812a00-8247-11eb-914a-cb113a44a5fd.png)
# Test
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.myapplication">

    <application
        android:allowBackup="true"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:roundIcon="@mipmap/ic_launcher_round"
        android:supportsRtl="true"
        android:theme="@style/Theme.MyApplication">
        <activity android:name=".Activity2"></activity>
        <activity android:name=".Activity1" />
        <activity android:name=".MainActivity">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
#main activity code
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;
import android.view.View;

import android.os.Bundle;

import com.google.android.material.floatingactionbutton.FloatingActionButton;

public class MainActivity extends AppCompatActivity {![Uploading Screenshot (8).png…]()

    public FloatingActionButton floatingActionButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        floatingActionButton=findViewById(R.id.editTextTextPersonName);
        floatingActionButton.setOnClickListener(new View.onClickListener(){
            @Override
            public void onClick(view v){
                Intent intent = new Intent (packageContext, MainActivity.this,Activity1.class);
                startActivity(intent);
            }
        });

    }
}
