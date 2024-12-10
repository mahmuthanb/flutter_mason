# Quick Start 💥

## 🎯 Activate from https://pub.dev
```
dart pub global activate mason_cli
```

## 📁 Initialize mason in the current workspace
```
mason init
```

## 📦 Install your first brick
```
mason add core --git-url https://github.com/mahmuthanb/flutter_mason --git-path ./bricks/core
mason add repository --git-url https://github.com/mahmuthanb/flutter_mason --git-path ./bricks/repository
mason add service --git-url https://github.com/mahmuthanb/flutter_mason --git-path ./bricks/service
mason add page --git-url https://github.com/mahmuthanb/flutter_mason --git-path ./bricks/page
mason get
```

## 📝 Code fix
```
dart fix --apply
```

## 🚧 Generate code from a brick
```
mason make core --name {app_name}
mason make page --name {page_name}
mason make repository --name {repository_name}
mason make service --name {service_name}
```

## 📱 Create needed platform codes 
You will see that you don't have any specific platform folders like android, ios.
Here you can automatically create these platform folders with this basic command.

``` 
flutter create .
```

> [!IMPORTANT]  
> This command will create missing platforms according to the flutter config that means default config comes with all platforms are genereted with upper command like macos, windows, linux, web. ([see below to change the config](#flutter-default-settings-disable-commands)) 

## Flutter default settings disable commands
You can simply create flutter project with the command below to see which platforms are generated default. 
```
flutter create sample_project
```
Then you can disable any platform with these commands to not to generating flutter create commands.

```
flutter config --no-enable-windows-desktop
```

### Other available flags: 

| Platform | Disable Command | Enable Command
| ----------- | ----------- | ----------- | 
| Windows Desktop   | --no-enable-windows-desktop   | --enable-windows-desktop
| MacOS Desktop     | --no-enable-macos-desktop     | --enable-macos-desktop
| Linux Desktop     | --no-enable-linux-desktop     | --enable-linux-desktop
| Web               | --no-enable-web               | --enable-web
| Android           | --no-enable-android           | --enable-android
| iOS               | --no-enable-ios               | --enable-ios
 
If you want to enable the paltform codes generation while working with flutter official cli command, you can use enable commands like 
```
flutter config --enable-windows-desktop
```

---

> You can check this commands from [official flutter website](https://docs.flutter.dev/platform-integration/desktop#create-a-new-project)


> Check official [mason-cli](https://docs.bymason.com/) and [brickhub](https://docs.brickhub.dev/) pages to be up-to-date

> Thanks for using bricks from my repo. You can star the repo to support me.