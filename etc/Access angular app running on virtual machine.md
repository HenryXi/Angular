# Access angular app running on virtual machine
I install Node.js and npm in my virtual machine which OS is CentOS. I following official website [here](https://angular.io/guide/quickstart)
to start my first Angular app. After execute `ng new my-app` init the project I execute `ng serve --open` to start the app.
The log is here.
```
[root@localhost my-app]# ng serve --open
** Angular Live Development Server is listening on localhost:4200, open your browser on http://localhost:4200/ **

Date: 2018-08-01T14:13:42.780Z
Hash: 041cde23e4fcb4e3d5e3
Time: 52040ms
chunk {main} main.js, main.js.map (main) 10.6 kB [initial] [rendered]
chunk {polyfills} polyfills.js, polyfills.js.map (polyfills) 227 kB [initial] [rendered]
chunk {runtime} runtime.js, runtime.js.map (runtime) 5.22 kB [entry] [rendered]
chunk {styles} styles.js, styles.js.map (styles) 15.6 kB [initial] [rendered]
chunk {vendor} vendor.js, vendor.js.map (vendor) 3.27 MB [initial] [rendered]
ℹ ｢wdm｣: Compiled successfully.
```
The ip of virtual machine is "192.168.56.6". When I access 192.168.56.6:4200 in my physical machine I got nothing. I read the log again and
google this issue. I use following command to start the app.
```
ng serve --host 0.0.0.0
```
Then I can access the page "192.168.56.6:4200" from my physical machine successfully.

EOF