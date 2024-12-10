Hello Kakao-groom DEV Bootcamp



CIRCLE MENU [JAVA]
A simple, elegant UI menu with a circular layout and material design animations
We specialize in the designing and coding of custom UI for Mobile Apps and Websites.

Stay tuned for the latest updates:


Twitter Codacy Badge Donate

Requirements
​

Android 4.1 Jelly Bean (API lvl 16) or greater
Your favorite IDE
Installation
​Just download the package from here and add it to your project classpath, or just use the maven repo:

Gradle:

implementation 'com.ramotion.circlemenu:circle-menu:0.3.2'
SBT:

libraryDependencies += "com.ramotion.circlemenu" % "circle-menu" % "0.3.2"
Maven:

<dependency>
	<groupId>com.ramotion.circlemenu</groupId>
	<artifactId>circle-menu</artifactId>
	<version>0.3.2</version>
</dependency>
​

Basic usage
Place the CircleMenuView in your layout and set the icons and colors of the buttons, as shown below.

app:button_colors="@array/colors"
app:button_icons="@array/icons"
Example of arrays colors and icons in res\values\buttons.xml:

<?xml version="1.0" encoding="utf-8"?>
<resources>
    <array name="icons">
        <item>@drawable/ic_home_white_24dp</item>
        <item>@drawable/ic_search_white_24dp</item>
        <item>@drawable/ic_notifications_white_24dp</item>
        <item>@drawable/ic_settings_white_24dp</item>
        <item>@drawable/ic_place_white_24dp</item>
    </array>
    <array name="colors">
        <item>@android:color/holo_blue_light</item>
        <item>@android:color/holo_green_dark</item>
        <item>@android:color/holo_red_light</item>
        <item>@android:color/holo_purple</item>
        <item>@android:color/holo_orange_light</item>
    </array>
</resources>
Or use the constructor

CircleMenuView(@NonNull Context context, @NonNull List<Integer> icons, @NonNull List<Integer> colors)
to add CircleMenuView and configure the buttons programmatically (in the code).

Next, connect the event handler CircleMenuView.EventListener as shown below, and override the methods you need.

final CircleMenuView menu = (CircleMenuView) findViewById(R.id.circle_menu);
menu.setEventListener(new CircleMenuView.EventListener() {
    @Override
    public void onMenuOpenAnimationStart(@NonNull CircleMenuView view) {
        Log.d("D", "onMenuOpenAnimationStart");
    }

    @Override
    public void onMenuOpenAnimationEnd(@NonNull CircleMenuView view) {
        Log.d("D", "onMenuOpenAnimationEnd");
    }

    @Override
    public void onMenuCloseAnimationStart(@NonNull CircleMenuView view) {
        Log.d("D", "onMenuCloseAnimationStart");
    }

    @Override
    public void onMenuCloseAnimationEnd(@NonNull CircleMenuView view) {
        Log.d("D", "onMenuCloseAnimationEnd");
    }

    @Override
    public void onButtonClickAnimationStart(@NonNull CircleMenuView view, int index) {
        Log.d("D", "onButtonClickAnimationStart| index: " + index);
    }

    @Override
    public void onButtonClickAnimationEnd(@NonNull CircleMenuView view, int index) {
        Log.d("D", "onButtonClickAnimationEnd| index: " + index);
    }
});
You can use open(boolean animate) and close(boolean animate) methods, to open and close menu programmatically

Here are the attributes you can specify through XML or related setters:

button_icons - Array of buttons icons.
button_colors - Array of buttons colors.
icon_menu - Menu default icon.
icon_close - Menu closed icon.
icon_color - Menu icon color.
duration_ring - Ring effect duration.
duration_open - Menu opening animation duration.
duration_close - Menu closing animation duration.
distance - Distance between center button and buttons

🗂 Check this library on other language:
 
📄 License
Circle Menu Android is released under the MIT license. See LICENSE for details.

This library is a part of a selection of our best UI open-source projects

If you use the open-source library in your project, please make sure to credit and backlink to www.ramotion.com

📱 Get the Showroom App for Android to give it a try
Try this UI component and more like this in our Android app. Contact us if interested.

 
