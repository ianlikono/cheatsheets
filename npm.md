# npm

#### Install a package to the local project

`npm install express`

#### Install a package to the local project and install it globally as well

`npm install -g express`

#### Install and save a package

Use the `--save` flag to update the package.json file automatically

`npm install express --save`

#### Remove a global package

`npm uninstall -g express`

#### Auto-update a dependency to a specific version

`npm install express@<version #> --save`

#### Set Your npm Author Info

You can either set them manually:

```
npm set init.author.name "Your Name"
npm set init.author.email "youremail@example.com"
npm set init.author.url "http://yoururl.com"
```

Or you can start the interactive prompt by typing:

`npm adduser`

#### Display Your npm Configuration Settings

`npm config ls`

#### See where the default npm directory is

`npm config get prefix`

#### List all global npm packages

`npm ls -g`



#### Articles

- [Why I Left Gulp and Grunt for npm Scripts](https://medium.com/@housecor/why-i-left-gulp-and-grunt-for-npm-scripts-3d6853dd22b8#.la6lykfzg)
