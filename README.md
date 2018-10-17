

### Bugfix

##### 1. Fixed shortcuts do not work in non-english input method for IDA7.1. Eg: F2, tab, ctrl+enter etc.

```
Replace the "libqcocoa.dylib" to 
/Applications/IDA Pro 7.1/ida.app/Contents/PlugIns/platforms/libqcocoa.dylib
```



##### Binary file checksum:

```
md5 libqcocoa.dylib
MD5 (libqcocoa.dylib) = 09ead6dd6d40a32ba1ec470f3b830ee3

shasum libqcocoa.dylib
b70d5dd983bbd852b1066318e84788279e8d08e2  libqcocoa.dylib
```



##### Recompile Qt5.6
##### **Download** 

```
https://download.developer.apple.com/Developer_Tools/Xcode_7.3.1/Xcode_7.3.1.dmg
```

##### **Switch**

```
sudo xcode-select -switch /Applications/Xcode7.app/Contents/Developer
```

**Compile argument**

```
sh configure "-nomake" "tests" "-qtnamespace" "QT" "-confirm-license" "-accessibility" "-opensource" "-force-debug-info" "-platform" "macx-g++" "-debug-and-release" "-fontconfig" "-qt-freetype" "-qt-libpng" "-qt-sql-sqlite" "-prefix" "Qt/5.6.3-x64"
```