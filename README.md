# easyCountDownTimer
A simple android library to countdown timer textview for api 14+

## Screan shot

![screan_shot](https://user-images.githubusercontent.com/6823491/30234511-0261af9c-9513-11e7-964b-b0f6c45f6261.gif)

## Setup

The simplest way to use easyCountDownTimer is to add the library as aar dependency to your build.

#### Maven

```
<dependency>
  <groupId>ir.samanjafari.easycountdowntimer</groupId>
  <artifactId>easycountdowntimer</artifactId>
  <version>1.1</version>
  <type>pom</type>
</dependency>
```

#### Gradle

```
repositories {
    maven {
             url 'https://dl.bintray.com/samanjafaridotir/easyCountDownTimerTextview'
          }
}

dependencies {
    compile 'ir.samanjafari.easycountdowntimer:easycountdowntimer:1.1'
}
```

#### Usage

Add the following code to your view

```xml
<ir.samanjafari.easycountdowntimer.EasyCountDownTextview
        android:id="@+id/easyCountDownTextview"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_centerInParent="true"
        app:hours="2"
        app:minute="2"
        app:second="15"
        app:showHours="false"
        app:textSize="25sp"
        app:textColor="#000"
        app:setAnimation="true"
        />
```

whit the following code you can listen to onFinish or onTick timer

```java
EasyCountDownTextview countDownTextview = (EasyCountDownTextview) findViewById(R.id.easyCountDownTextview);
countDownTextview.setOnTick(new CountDownInterface() {
            @Override
            public void onTick(long time) {
                Log.i("main activty", "onTick");
            }

            @Override
            public void onFinish() {
                Log.i("main activity", "onFinish");
            }
        });
```


