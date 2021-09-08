# React-native-razorpay-integration
This repo is for Payment integration. React Native Razorpay integration very easy and simple way for Android and iOS both.

===========================================
Step 1: Install Razorpay React Native SDK🔗
Install the SDK using the following npm command in the Terminal window. If you are using Windows, please use Git Bash instead of Command Prompt window. Ensure that you run this code within your React Native project folder in Terminal window.

>>>> npm install react-native-razorpay --save

===========================================

==========================================================
Step 2: Import Razorpay Package in MainApplication.java🔗
Launch Android Studio and open the MainAplication.java file from your project folder. Add the following code:

>>>> import com.razorpay.rn.RazorpayPackage;

Also, add new RazorpayPackage() to the list returned by the getPackages() method.

 >>>> protected List<ReactPackage> getPackages() {
    @SuppressWarnings("UnnecessaryLocalVariable")
    List<ReactPackage> packages = new PackageList(this).getPackages();
    // Packages that cannot be autolinked yet can be added manually here, for example:
        packages.add(new RazorpayPackage());
        return packages;
}

===========================================================

===========================================================
Step 3: Add Razorpay SDK in Settings Gradle File🔗
Append the following lines to the settings.gradle file.

>>>> include ':react-native-razorpay'
project(':react-native-razorpay').projectDir = new File(rootProject.projectDir,   '../node_modules/react-native-razorpay/android')

===========================================================

===========================================================
Step 4: Add Dependency in App Build Gradle File🔗
Add the following lines in the dependencies section of your app's build.gradle file.

>>>> implementation project(':react-native-razorpay')

===========================================================

=================================
Step 5: Run React Native App🔗
Run the React Native app.

>>>> npx react-native run-android
=================================
