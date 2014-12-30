## Install for production
-------------------------
- install stpa-modal running the following command

```shell
$ bower install stpa-modal --save
```

- **Note:** if you are asked about `Unable to find a suitable version for angular` answer `angular#1.3.x which is required by stpa-modal`.
- **Note:** if you are issued about `github.com connection timed out` just run `git config --global url.https://.insteadOf git://` in terminal.

- include `stpa-modal.min.js` on your project. It should be located at `bower_components/stpa-modal/src`

```html
<script src="../bower_components/stpa-modal/src/stpa-modal.min.js"></script>
```

- add `stpa.modal` and `ui.bootstrap` as a module dependency to your app

```js
angular.module('my.app', [
    'stpa.modal',
    'ui.bootstrap'
])
```


## Usage
--------

- insert `<stpa-modal></stpa-modal>` directive into your template

```html
<stpa-modal body="<h1>Hello World!</h1>">Open Modal</stpa-modal>
```

Check out [documentation](https://modal.stpa.co) for more examples

## Install for development
--------------------------
- install node and bower on your environment
- cd to your development folder and clone repo

```sh
$ git clone https://github.com/stpa-co/stpa-modal.git stpa-modal
$ cd stpa-modal
```

- install module dependencies

```sh
$ npm install
$ bower install
```

- **Note:** if you are issued about `github.com connection timed out` just run `git config --global url.https://.insteadOf git://` in terminal.

- serve project and do the work

```sh
$ gulp serve #Note: maybe you should have to use `sudo`
```

- serve project on distribution mode

```sh
$ gulp serve:dist #Note: maybe you should have to use `sudo`
```

- build project to distribution

```sh
$ gulp build #Note: maybe you should have to use `sudo`
```

**Note:** running the command `gulp build` should generate minified src at `src/stpa-modal.min.js`, and the docs on `dist/doc` folder.

**Note:** running the command `gulp serve` should serve on `http://localhost:3000/doc` with live reload. It also should watch the changes to re-build all the things, generating minified src at `src/stpa-modal.min.js`, and docs on `dist/doc` folder.

**Note:** running the command `gulp serve:dist` should do the same above but with all bower dependencies minified.

**Note:** to update project src please open an issue, fork the project, do your work, run `gulp build` and make a pull-request. thx =D 

**Note:** to update docs just run `gulp build` or `./buil.sh`, and make a pull-request into `gh-pages` branch only with contents of `dist/doc` folder. I like to work with another folder only for the docs (pointing to the same remote), maybe you will also. You can use the `build.sh` script located in the root to automate the process, but check it before.

**Note** Also check the tasks located on gulp folder for more details.

Feel free to open issues if you run into a problem or if you just have suggestions. Pull Requests are always welcome.

## License
---------------
The `stpa-modal` is open-sourced software licensed under the [MIT](http://opensource.org/licenses/MIT) license. Created by [@stewones](https://twitter.com/stewones)