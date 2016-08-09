#OCaml Node JSONFile

## What is ocaml-node-jsonfile?

ocaml-node-jsonfile is a binding to the node module jsonfile. It will let you use its functions directly in ocaml

## How to install?

You need to switch to ocaml **4.03.0**:
`opam switch 4.03.0`

First, you need to install [ocaml-node](https://github.com/besport/ocaml-node.git) if you haven't already installed it

To install this packae use the command:
`opam pin add ocaml-node-jsonfile https://github.com/besport/ocaml-node-jsonfile.git`

## How to use?

Here is an example:

Javascript code:

```JavaScript
var jsonfile = require("jsonfile");
var obj = {name: "OCaml"};
jsonfile.writeFileSync("file.json", obj);
```

Equivalent in OCaml using gen_js_api (for Ojs.t type):

```OCaml
let jsonfile = Node.require "jsonfile" in
let obj = Ojs.empty () in
let obj = Ojs.set obj "name" (Ojs.string_to_js "OCaml") in
Node_jsonfile.write_file_sync jsonfile "file.json" obj
```

## What about the full documentation?
 
You can find the full documentation of `jsonfile` on the github repo:  
https://github.com/jprichardson/node-jsonfile