# ios-working-with-sandbox-plugin
Plugin used for testing sandbox-pod and pod support in nativescript-cli.
This plugin will try to create file called `I_MADE_THIS_FILE.txt` in `<project_name>/platforms/app/` directory.
The build `.ipa` should contain this file.

## How to use

### NativeScript CLI:
In your project execute:
```
$ tns plugin add not-whlist-sandox-plugin
```

or add the following entry in your `package.json`:

```JSON
"dependencies": {
	"not-whlist-sandox-plugin": "1.0.0"
}
```

### AppBuilder
Add the following entry in your `package.json`:

```JSON
"dependencies": {
	"not-whlist-sandox-plugin": "1.0.0"
}
```

### AppBuilder CLI
In your project execute:
```
$ appbuilder plugin add not-whlist-sandox-plugin
```

or add the following entry in your `package.json`:

```JSON
"dependencies": {
	"not-whlist-sandox-plugin": "1.0.0"
}
```

## Expected result when building the project

### NativeScript CLI
In the default scenario the build should succeed and the build `.ipa` must contain the `I_MADE_THIS_FILE.txt` file. The file should be created in `<project_dir>/platforms/ios/<project_name>/app/`.

In case you open `<cli_install_dir>/config/config.json` and set `USE_POD_SANDBOX` to `false`, the build should do the same.

### AppBuilder
In the default scenario the build should succeed and the build `.ipa` must contain the `I_MADE_THIS_FILE.txt` file.
The build will fail in case this plugin is not whitelisted.
