# [SwiftLintDemo](https://betterprogramming.pub/improving-swift-code-readability-with-swiftlint-a3459e968c4b)

## 1. Install SwiftLint
```
brew install swiftlint
```

You can now run swiftlint in terminal. At the root of your project run the following:
```
swiftlint
```

By default, SwiftLint is applying Raywenderlich’s Swift Style Guide. 

## 2. Configuring SwiftLint
[To configure swiftlint](https://github.com/realm/SwiftLint#configuration) we must create a configuration file at the root of our project. The file must be named .swiftlint.yml
```
touch .swiftlint.yml
```

### Example
To disable rules add the following to your .swiftlint.yml:
```
disabled_rules:
- void_return
- trailing_whitespace
- line_lengt
```

## 3. Running SwiftLint during the Xcode build process
### Select Build Phases tab (Project settings > App target > Build Phases)
<img width="1512" src="https://user-images.githubusercontent.com/47273077/158492192-b39209d4-32a8-4c8e-8303-293af3654048.png">

### Click on the “+” button then select “New Run Script Phase”. Name the run script phase “Run SwiftLint” and paste the following code:
```
export PATH="$PATH:/opt/homebrew/bin"

if which swiftlint >/dev/null; then
  swiftlint
else
  echo "warning: SwiftLint not installed, download from https://github.com/realm/SwiftLint"
fi
```
<img width="850" src="https://user-images.githubusercontent.com/47273077/158492442-518dc63c-62d3-4b2e-b7db-f46c3c735e93.png">



