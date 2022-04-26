Ref : 
* https://blog.chainsafe.io/an-intro-to-the-sauron-web-framework-a6093a2ac9eb

Compile the project by issuing the following command at the root folder of your project:
wasm-pack build --release --target=web

A folder ./pkg is then created inside our project directory. This contains the resulting compiled files. We only need to pay attention to two files, with their filename derived from the given package name <package_name>.js and <package_name>_bg.wasm. In this case, we will have counter.js and counter_bg.wasm.

Finally, serve the files using basic-http-server.
basic-http-server -a 0.0.0.0:4000
Then navigate your browser to http://localhost:4000 to see and interact with the app.
