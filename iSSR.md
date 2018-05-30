# Shadow Socks for iOS

```
git clone https://github.com/haxpor/Potatso.git --depth=1 iSSR && cd iSSR
```

```
git submodule update --init --recursive
```

```
sudo gem install cocoapods && pod install
```

```
If Error Occurs:
pod cache clean Realm
pod cache clean RealmSwift
pod deintegrate || rm -rf Pods
pod install --verbose
```

```
It seems I found the Error, Itself, Manually do this Below.
===========================================================
mkdir -p ~/.cocoapods/repos && cd ~/.cocoapods/repos
git clone https://github.com/CocoaPods/Specs.git master
===========================================================
Then Re-Run the Steps above.
```

```
# SKIP
cd Library/openssl
```

```
# SKIP
./build-libssl.sh
```

```
open Potatso.xcworkspace
```
