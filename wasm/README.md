## WASM (Webassembly) support

**Important note: to run the Webassembly demo at least Go 1.13 is required!**

Starting from **v1.4.0** Pigo has been ported to Webassembly 🎉. This gives a huge gain in terms of real time performance.

This means that there is no need anymore to run the library in a Python environment as a shared library. For more details check the project description from the [Readme](https://github.com/esimov/pigo/blob/master/README.md#real-time-face-detection) file and also this [blog post](https://esimov.com/2019/11/pupilseyes-localization-in-the-pigo-face-detection-library).

## How to run it?

Download and build the [serve](https://github.com/mattn/serve) package for making a simple webserver. Then simply type the `$ make` to build the `wasm` file and to start the webserver. That's all. It will open a new page in your browser on the following address `http://localhost:5000/`.

In case the `lib.wasm` is not generated automatically you can build yourself by running the following command:

```bash
$ GOOS=js GOARCH=wasm go build -o lib.wasm wasm.go
```
### Supported keys:
<kbd>s</kbd> - Show/hide pupils<br/>
<kbd>c</kbd> - Toggle circle/rectangle detection mark<br/>
<kbd>f</kbd> - Show/hide facial landmark points (hidden by default)

## Face masquerading demo

This folder also contains a demo showing an example how the library can be used to create a Snapchat like face masquerading effect. You can run the example by typing the following command:

```bash
$ make demo
```

---
### Snapshot from the running demo

![masquerade](https://user-images.githubusercontent.com/883386/78139722-a04f6a00-7431-11ea-9adb-86d69cb3c73f.png)

