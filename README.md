

### IDA7.1_SP

##### 1. Fixed shortcuts do not work in non-english input method for IDA7.1. Eg: F2, tab, ctrl+enter etc.
##### 2. Added load bundle for open dialog (The official Qt does not support this feature, but this is suitable for ida )


```
Replace the "libqcocoa.dylib" to 
/Applications/IDA Pro 7.1/ida.app/Contents/PlugIns/platforms/libqcocoa.dylib
```



##### Binary file checksum:

```
md5 libqcocoa.dylib
MD5 (libqcocoa.dylib) = 310883a9e06c16a126d1e2e6918a513c

shasum libqcocoa.dylib
f9dbe925262ac9b79ca1c5d4a9423efaa00d5e7f  libqcocoa.dylib
```



##### Recompile Qt5.6.3
##### **Download (Xcode10 supported)** 

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
