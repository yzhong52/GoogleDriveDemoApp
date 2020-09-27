# Google Drive Demo App

This the demo code for https://medium.com/p/9207e4cb05ba.

# Firebase 

## iOS Configuration

This is not covered by the blog post. But it is similar to the Android configuration.
We won't go into details here. But in a nutshell:

In Firebase project settings, add clicked on add Firebase to iOS app.

Make sure the bundle identifier matches what you have in the Xcode project file. 

Download the `GoogleService-Info.plist` and add it to the Xcode project.

Add the following section to `Info.plist`. The `com.demo.googledrivedemoapp` should match the bundle identifier from the Xcode project. And the `com.googleusercontent.apps.1029621683798-t85vtsmj8v1uujg29888dv6f8vblnrs8` string should match the value of `REVERSED_CLIENT_ID` in the `GoogleService-Info.plist` file above.

```
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
 <key>CFBundleURLTypes</key>
 <array>
     <dict>
         <key>CFBundleTypeRole</key>
         <string>Editor</string>
         <key>CFBundleURLSchemes</key>
         <array>
             <string>com.demo.googledrivedemoapp</string>
         </array>
     </dict>
     <dict>
         <key>CFBundleTypeRole</key>
         <string>Editor</string>
         <key>CFBundleURLSchemes</key>
         <array>
             <string>com.googleusercontent.apps.1029621683798-t85vtsmj8v1uujg29888dv6f8vblnrs8</string>
         </array>
     </dict>
 </array>
```