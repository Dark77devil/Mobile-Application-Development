# Ex.No: 11 Develop a application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio.


## AIM:

To develop a application to add animation to imageview,move,blink,fade,clockwise,zoom,slide operation using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “animation″ and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Design other operations layout in respective .xml files.

Step 7: Get images details and Add animations in MainActivity file.

Step 8: Save and run the application.

## PROGRAM:
```
/*
Program to display animation operation”.
Developed by: M MANO
Registeration Number : 212221040100
*/
```
**Activity_xml File:**

    <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:backgroundTint="#4CAF50"
    tools:context=".MainActivity">

    <ImageView
        android:id="@+id/imageView"
        android:layout_width="320dp"
        android:layout_height="212dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.494"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.148"
        app:srcCompat="@drawable/imn" />

    <Button
        android:id="@+id/BTNblink"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:backgroundTint="#4CAF50"
        android:text="BLINK"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.535"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.538" />

    <Button
        android:id="@+id/BTNrotate"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:backgroundTint="#4CAF50"
        android:text="ROTATE"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.153"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.538" />

    <Button
        android:id="@+id/BTNfade"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:backgroundTint="#4CAF50"
        android:text="FADE"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.535"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.642" />

    <Button
        android:id="@+id/BTNmove"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:backgroundTint="#4CAF50"
        android:text="MOVE"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.151"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.642" />

    <Button
        android:id="@+id/BTNslide"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:backgroundTint="#4CAF50"
        android:text="SLIDE"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.897"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.538" />

    <Button
        android:id="@+id/BTNzoom"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:backgroundTint="#4CAF50"
        android:text="ZOOM"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.897"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.642" />

    <Button
        android:id="@+id/BTNstop"
        android:layout_width="380dp"
        android:layout_height="51dp"
        android:backgroundTint="#F44336"
        android:text="STOP ANIMATION"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.516"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.772" />

    </androidx.constraintlayout.widget.ConstraintLayout>

**Blink.xml:**
      
    <?xml version="1.0" encoding="utf-8"?>
    <set xmlns:android="http://schemas.android.com/apk/res/android">
    <alpha android:fromAlpha="0.0"
        android:toAlpha="1.0"
        android:interpolator="@android:anim/accelerate_interpolator"
        android:duration="500"
        android:repeatMode="reverse"
        android:repeatCount="infinite"/>
    </set>

**Fade.xml:**

    <?xml version="1.0" encoding="utf-8"?>
    <set xmlns:android="http://schemas.android.com/apk/res/android">
    <!-- duration is the time for which animation will work-->
    <alpha
        android:duration="1000"
        android:fromAlpha="0"
        android:toAlpha="1" />
    <alpha
        android:duration="1000"
        android:fromAlpha="1"
        android:startOffset="2000"
        android:toAlpha="0" />
    </set>

**Move.xml:**
 
      <?xml version="1.0" encoding="utf-8"?>
    <set xmlns:android="http://schemas.android.com/apk/res/android">
    <translate
        android:fromXDelta="0%p"
        android:toXDelta="75%p"
        android:duration="700" />
    </set>

**Rotate.xml:**

      <?xml version="1.0" encoding="utf-8"?>
    <set xmlns:android="http://schemas.android.com/apk/res/android">
    <rotate
        android:duration="6000"
        android:fromDegrees="0"
        android:pivotX="50%"
        android:pivotY="50%"
        android:toDegrees="360" />

    <rotate
        android:duration="6000"
        android:fromDegrees="360"
        android:pivotX="50%"
        android:pivotY="50%"
        android:startOffset="5000"
        android:toDegrees="0" />
    </set>

**Slide.xml:**

      <?xml version="1.0" encoding="utf-8"?>
    <set xmlns:android="http://schemas.android.com/apk/res/android">
    <scale
        android:duration="500"
        android:fromXScale="1.0"
        android:fromYScale="1.0"
        android:interpolator="@android:anim/linear_interpolator"
        android:toXScale="1.0"
        android:toYScale="0.0" />
    </set>

**Zoom.xml:**

    <?xml version="1.0" encoding="utf-8"?>
    <set xmlns:android="http://schemas.android.com/apk/res/android">
    <scale xmlns:android="http://schemas.android.com/apk/res/android"
        android:fromXScale="0.5"
        android:toXScale="3.0"
        android:fromYScale="0.5"
        android:toYScale="3.0"
        android:duration="1000"
        android:pivotX="25%"
        android:pivotY="25%" >
    </scale>
    <scale xmlns:android="http://schemas.android.com/apk/res/android"
        android:startOffset="1000"
        android:fromXScale="3.0"
        android:toXScale="0.5"
        android:fromYScale="3.0"
        android:toYScale="0.5"
        android:duration="1000"
        android:pivotX="25%"
        android:pivotY="25%" >
    </scale>
    </set>

**MainActivity.java File:**
    
    package com.example.graphicsimplier;

    import androidx.appcompat.app.AppCompatActivity;

    import android.os.Bundle;
    import android.view.View;
    import android.view.animation.Animation;
    import android.view.animation.AnimationUtils;
    import android.widget.Button;
    import android.widget.ImageView;

    public class MainActivity extends AppCompatActivity {
    ImageView imageView;
    Button blinkBTN, rotateBTN, fadeBTN, moveBTN, slideBTN, zoomBTN, stopBTN;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        imageView = findViewById(R.id.imageView);
        blinkBTN = findViewById(R.id.BTNblink);
        rotateBTN = findViewById(R.id.BTNrotate);
        fadeBTN = findViewById(R.id.BTNfade);
        moveBTN = findViewById(R.id.BTNmove);
        slideBTN = findViewById(R.id.BTNslide);
        zoomBTN = findViewById(R.id.BTNzoom);
        stopBTN = findViewById(R.id.BTNstop);

        blinkBTN.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // To add blink animation
                Animation animation = AnimationUtils.loadAnimation(getApplicationContext(), R.anim.blink);
                imageView.startAnimation(animation);
            }
        });

        rotateBTN.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // To add rotate animation
                Animation animation = AnimationUtils.loadAnimation(getApplicationContext(), R.anim.rotate);
                imageView.startAnimation(animation);
            }
        });
        fadeBTN.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // To add fade animation
                Animation animation = AnimationUtils.loadAnimation(getApplicationContext(), R.anim.fade);
                imageView.startAnimation(animation);
            }
        });
        moveBTN.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // To add move animation
                Animation animation = AnimationUtils.loadAnimation(getApplicationContext(), R.anim.move);
                imageView.startAnimation(animation);
            }
        });
        slideBTN.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // To add slide animation
                Animation animation = AnimationUtils.loadAnimation(getApplicationContext(), R.anim.slide);
                imageView.startAnimation(animation);
            }
        });
        zoomBTN.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // To add zoom animation
                Animation animation = AnimationUtils.loadAnimation(getApplicationContext(), R.anim.zoom);
                imageView.startAnimation(animation);
            }
        });
        stopBTN.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                // To stop the animation going on imageview
                imageView.clearAnimation();
            }
        });
    }

    }

## OUTPUT:
![image](https://github.com/Dark77devil/Mobile-Application-Development/assets/115543366/be4ca521-a0ac-4483-9bda-9c99e323d63d)  
![image](https://github.com/Dark77devil/Mobile-Application-Development/assets/115543366/38b771c5-c5d6-4772-93b4-4a4f8e569199)  
![image](https://github.com/Dark77devil/Mobile-Application-Development/assets/115543366/0a687288-1be1-4a21-9a3c-19a090d66bfd)  
![image](https://github.com/Dark77devil/Mobile-Application-Development/assets/115543366/a022907f-9bc4-4e4a-a9d7-ccc9322b3ece)  
![image](https://github.com/Dark77devil/Mobile-Application-Development/assets/115543366/227ede33-8384-40fb-a830-40ba922d000f)


## RESULT:

Thus the application to add animations to ImageView,Move,blink,fade,clockwise,zoom,slide operations are perform in android studio is created successfully.
