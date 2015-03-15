# adet
Automatically exported from code.google.com/p/adet

<h1><a name="Android_Drawable_Extension_Toolkit"></a>Android Drawable Extension Toolkit<a href="#Android_Drawable_Extension_Toolkit" class="section_anchor"></a></h1><p>Do you want android support SVG natively? Have you ever thought define your custom XML drawables? ADET(Android Drawable Extension Toolkit) could solve these problems, use ADET, you can use SVG as a <strong>REAL</strong> drawable for any scenarios, such as use SVG for an android <strong>NATIVE ImageView</strong> src attribute. or even define your custom XML drawables to enhance and replace the ordinary simple shape drawable in android. </p><p>adet use <a href="http://code.google.com/p/svg-android-2" rel="nofollow">svg-android-2</a> as it&#x27;s svg library. Why didn&#x27;t I use <a href="/p/adet/wiki/LibSvgAndroid">LibSvgAndroid</a>? Because the lib has an annoying bug that crash apps in some circumstance. </p><p>All in all, ADET can extend and enhance android drawable system. </p><p>the screen shot demonstrates a very popular SVG file named lion<br></br> <img src="http://adet.googlecode.com/svn/trunk/AdetSample/screenshots/screen_shot.jpg" /> </p><h1><a name="Simple_to_Use"></a>Simple to Use<a href="#Simple_to_Use" class="section_anchor"></a></h1><ol><li>Just reference ADET as an Android library <br></br> </li><li>Create a class(such as MyApp) which extends Application <br></br> </li><li>in MyApp write this code below: </li><pre class="prettyprint">public class MyApp extends Application {

	@Override
	public void onCreate() {
		super.onCreate();
		// call this init method at your application once, and we done!
		ADET.init(getApplicationContext());
	}
}</pre><li>Don&#x27;t forget to modify <a href="https://code.google.com/p/adet/source/browse/trunk/AdetSample/AndroidManifest.xml" rel="nofollow">AndroidManifest.xml</a> </li><pre class="prettyprint">    &lt;application
        android:name=&quot;MyApp&quot; 
        android:label=&quot;@string/app_name&quot;
        android:icon=&quot;@drawable/ic_launcher&quot;
        android:theme=&quot;@style/AppTheme&quot;&gt;
    &lt;/application&gt;</pre><li>Put some SVG files into res/drawable folder, and then you can use these SVG files as <strong>native</strong> drawables in anywhere! the fellowing xml contents are part of <a href="https://code.google.com/p/adet/source/browse/trunk/AdetSample/res/layout/adet_demo_layout.xml" rel="nofollow">adet_demo_layout.xml</a>: </li><pre class="prettyprint">    &lt;ImageView
          android:layout_width=&quot;fill_parent&quot;
          android:layout_height=&quot;fill_parent&quot;
          android:layout_gravity=&quot;center&quot;
          android:background=&quot;#FF806440&quot;
          android:scaleType=&quot;fitXY&quot;
          android:src=&quot;@drawable/lion&quot; /&gt;</pre></ol><p>Simple! isn&#x27;t it? Using SVG in android has never been so easy before ;-) </p>
