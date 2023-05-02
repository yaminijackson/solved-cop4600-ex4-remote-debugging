Download Link: https://assignmentchef.com/product/solved-cop4600-ex4-remote-debugging
<br>
<strong>Ex4: Remote Debugging </strong>

Often we need or want to debug software on a remote host via a network debugger. Android (and Reptilian) has a built-in remote debugging system to facilitate development at the Java and native (C/C++) layers. In this project, you will use the network debugging system to push and test a simple Android application on Reptilian. The skills learned will be used in upcoming projects. You will take screenshots of app’s results. You’ll submit screenshots as well your source file on Canvas.

<h1>Structure</h1>

The exercise can be completed as follows:




<ul>

 <li>Install Android Studio 4.0.1 (or later), SDK, and NDK</li>

 <li>Add functionality to the skeleton GUI project provided (see specification below) 3) Build and remotely test (via Android remote debugging / LLDB) application 4) Submit your source file and your screenshots on Canvas.</li>

</ul>




Reptilian has remote debugging built in, but in order to connect to this system, the VM must port-forward to the local host. In the latest version of Reptilian, this forwarding is already set up for you.

<h1>Android Studio</h1>

Android Studio is set up to quickly and easily connect to the remote debugging system on Android devices. In this exercise, you’ll install Android Studio 4.0.1, the Software Development Kit (SDK), the Native Development Kit (NDK), and several tools.




You can download Android Studio from here: <a href="https://developer.android.com/studio/index.html">https://developer.android.com/studio/index.html</a><a href="https://developer.android.com/studio/index.html">.</a> You do not need to install the “Android Virtual Device” (though you may if you’d like). On the first run, you’ll be prompted to download and install elements of the SDK and support tools. <strong>This will take some time!</strong>




Once Android Studio starts, in top ribbon menu, do the following to install the rest of the necessary software:




<ul>

 <li>Click Tools → SDK Manager</li>

 <li>Under “SDK Platforms”, add “Android 9.0 (Pie)” 3) Under “SDK Tools”, add “CMake”, and “NDK”.</li>

</ul>

4) Click “Apply” to install the added software.










To connect Android Studio to Reptilian, you will need to connect VMware to Android Studio’s ADB instance. Navigate to Android Studio’s terminal and run the following command:




<strong>$</strong> <strong>[Path to ADB] connect [IP Address] </strong>

<strong> </strong>

For example, your path to ADB may look like the following:




<h2>$ C:Users[Username]AppDataLocalAndroidSdkplatform-toolsadb.exe</h2>

The ADB executable can generally be found in the path to the Android SDK Location, under “platformtools”.










Afterwards, your Reptilian instance will appear as a device labeled as “<strong>VMWare, Inc. VMWare Virtual Platform</strong>”.

<h1>Application</h1>

A skeleton Java project is provided for you to work with. We have also included a Kotlin project (a new

“blessed” Android language), but please know that this is just for fun – it <strong>is not supported</strong>, so TAs and the instructor may not be able to help you with problems. (We’ll try though!)




The skeleton project includes two text boxes – <strong>leftText</strong> and <strong>rightText</strong> – and two buttons – <strong>leftButton</strong> (labelled “Copy to Right”) and <strong>rightButton</strong> (labelled “Copy to Left”).




You must add code to the skeleton project so that, when <strong>leftButton</strong> is clicked, the text in <strong>leftText</strong> is copied to <strong>rightText</strong>, and when <strong>rightButton</strong> is clicked, rightText is copied to leftText. You should then test your application on Reptilian (via the Android Studio debugger) and take a screenshot of the application running in debug mode with both the Reptilian GUI and Android Studio debugger running.


