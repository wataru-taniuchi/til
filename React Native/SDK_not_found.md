# Android SDKが見つからない
> SDK location not found. Define location with sdk.dir in the local.properties file or with an ANDROID_HOME environment variable.

このエラーが出てきたら、ANDROID_HOMEが未設定のため設定してあげる。

#### 1. Android StudioからSDKの確認
1. Android Studio起動
2. [Preferences]
3. [Appearrance & Behavior]
4. [System Settings]
5. [Android SDK]
6. [Android SDK Location]

#### 2. ANDROID_HOMEの設定
1. `export ANDROID=$HOME/Library/Android/sdk`

* ~/.bash_profile に書いてもOK