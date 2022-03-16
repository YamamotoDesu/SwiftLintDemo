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
