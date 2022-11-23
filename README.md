# Cheat-Sheet

# Release build with command
./gradlew assemble release


# Test Card
Visa:4111111111111111
MasterCard:5431111111111111
Discover:6011601160116611


# Android bundle command
npx react-native bundle --dev false --platform android --entry-file index.js --bundle-output ./android/app/src/main/assets/index.android.bundle --assets-dest ./android/app/build/intermediates/res/merged/debug


# iOS build command
npx react-native bundle --entry-file index.js --platform ios --dev false --bundle-output ios/main.jsbundle --assets-dest ios


# Opening android studio at root location
cd /Applications/Android\ Studio.app/Contents/MacOS/
sudo ./studio


# Open Visual Studio Code at root location
sudo /Applications/Visual\ Studio\ Code.app/Contents/MacOS/Electron
sudo /Applications/Visual\Studio\Code.app/Contents/MacOS/Electron


# Android x error
npx jetify 


# For upgrading react-native project
React-native upgrade


#Port change command
react-native start —port 8088


# Keytool command 
keytool -list -v -keystore /Users/a123/Documents/React_Native/healthKit/android/app/healthKit -alias key0 -keyalg RSA -keysize 2048 -validity 10000


# Add to new project on android side
android:screenOrientation="portrait"
android:configChanges="keyboard|keyboardHidden|orientation|screenSize"
android:windowSoftInputMode="adjustResize"
android:launchMode="singleTask"


# Pod Install cmd for M1
 sudo arch -x86_64 gem install ffi
 arch -x86_64 pod install


# For Images not showing iOS
react-native/Libraries/Image/RCTUIImageViewAnimated.m
 if (_currentFrame) {
    layer.contentsScale = self.animatedImageScale;
    layer.contents = (__bridge id)_currentFrame.CGImage;
  } else {
    [super displayLayer:layer];
  }


# Image Issue for iOS 14 or above:
 else {
    [super displayLayer:layer];
  }

post_install do |installer|
    find_and_replace("../node_modules/react-native/Libraries/Image/RCTUIImageViewAnimated.m",
    "_currentFrame.CGImage;","_currentFrame.CGImage ;} else { [super displayLayer:layer];")
end
