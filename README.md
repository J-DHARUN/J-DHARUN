### Hi there 👋

<!--
**J-DHARUN/J-DHARUN** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->


<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
android:background="#FFFF8D"
tools:context=".MainActivity">
<TextView
android:id="@+id/textView"
android:layout_width="78dp"
android:layout_height="wrap_content"
android:layout_alignParentStart="true"
android:layout_alignParentLeft="true"
android:layout_alignParentTop="true"
android:layout_marginStart="35dp"
android:layout_marginLeft="35dp"
android:layout_marginTop="190dp"
android:layout_marginEnd="20dp"
android:layout_marginRight="20dp"
android:layout_marginBottom="20dp"
android:text="NAME"
android:textSize="20sp" />
<EditText
android:id="@+id/editName"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentTop="true"
android:layout_alignParentEnd="true"
android:layout_alignParentRight="true"
android:layout_marginTop="179dp"
android:layout_marginEnd="30dp"
android:layout_marginRight="30dp"
android:ems="10"
android:hint="Enter Name"
android:inputType="textPersonName" />
<Button
android:id="@+id/buttonSubmit"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_centerInParent="true"
android:text="SUBMIT" />
<TextView
android:id="@+id/tvResult"
android:layout_width="wrap_content"
android:layout_height="wrap_content"
android:layout_alignParentStart="true"
android:layout_alignParentLeft="true"
android:layout_alignParentBottom="true"
android:layout_marginStart="5dp"
android:layout_marginLeft="5dp"
android:layout_marginBottom="215dp"
android:textSize="30sp" />
</RelativeLayout>

java

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
import androidx.appcompat.app.AppCompatActivity;
public class MainActivity extends AppCompatActivity {
// These are the global variables
EditText editName;
TextView result;
Button buttonSubmit;
@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);
editName = (EditText) findViewById(R.id.editName);
result = (TextView) findViewById(R.id.tvResult);
buttonSubmit = (Button) findViewById(R.id.buttonSubmit);
/*
Submit Button
*/
buttonSubmit.setOnClickListener(new View.OnClickListener() {
@Override
public void onClick(View v) {
String name = editName.getText().toString();
result.setText("Welcome \t" + name );
}
});
}
}
