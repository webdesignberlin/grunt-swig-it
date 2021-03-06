# grunt-swig-it

> Create static HTML files using Swig

## Getting Started
This plugin requires Grunt `0.4.1`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-swig-it --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-swig-it');
```

## The "swig_it" task

### Overview
In your project's Gruntfile, add a section named `swig_it` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  swig_it: {
    dev: {
      options: {
        swigDefaults: {
          allowErrors: false,
          autoescape: true
        },
        data: {
          foo: {
            bar: 'yeah'
          }
        }
      },
      src: ['test/fixtures/**/*.html'],
      dest: "test/dest"
    }
  }
});
```

For each template found within src swig-it will look for a json file of the same name to use as data for the template.

The src directory should not include layout files so store 'pages' in a different folder to 'layouts' for your convenience.

If you store data inside `global.json`, placed in the root, this will be merged with any 'data' that you put inside the swig_it config.

## Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com/).
