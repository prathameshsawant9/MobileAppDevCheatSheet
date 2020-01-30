# Android Security

 #### This shows the activity as blank/blur in recent apps of android :
```java
getWindow()
.setFlags(WindowManager.LayoutParams.FLAG_SECURE, 
                     WindowManager.LayoutParams.FLAG_SECURE);
```

#### To remove from recent list when shutting down :
```java
finishAndRemoveTask();
```
##### Example : 
```java 
void onBackPressed(){
  finishAndRemoveTask();
  super.onBackPressed();
}
```
