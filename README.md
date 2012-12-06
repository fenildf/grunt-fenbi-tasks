# grunt-fenbi-tasks

Fenbi grunt tasks. To build handlebars template, combine [SeaJS] modules, generate jsctags, etc.

## Getting Started
Install the module with: `npm install grunt-fenbi-tasks`

```javascript
grunt.initConfig({
    handlebars: {
        development: {
            src: SOURCE,
            dest: TARGET_SOURCE,
            files: '**/*.handlebars',
            templateModule: 'util/Template'
        },
        release: {
            src: TEMP_SOURCE,
            dest: TEMP_SOURCE,
            files: '**/*.handlebars',
            templateModule: 'util/Template'
        }
    },

    cdn: {
        test: {
            src: TEMP_BUILD,
            dest: TARGET_RELEASE,
            urlPrefix: '/s/',
            files: '**/*.*',
            staticMap: TARGET + 'WEB-INF/view/global/StaticMap.vm'
        },

        production: {
            src: TEMP_BUILD,
            dest: TARGET + 's/',
            urlPrefix: '//cdn.yuanti.ku/s/',
            files: '**/*.*',
            staticMap: TARGET + 'WEB-INF/view/global/StaticMap.vm'
        }
    },

    jsctags: {
        development: {
            root: SOURCE,
            files: [
                'bootstrap/**/*.js',
                'collection/**/*.js',
                'component/**/*.js',
                'global/**/*.js',
                'model/**/*.js',
                'page/**/*.js',
                'router/**/*.js',
                'task/**/*.js',
                'util/**/*.js'
            ]
        }
    },

    combo: {
        release: {
            src: TEMP_SOURCE,
            dest: TEMP_BUILD,
            bootstrap: 'bootstrap/**/*.js',
            loader: 'loader.js'
        }
    }
});
```

## Documentation
_(Coming soon)_

## Examples
_(Coming soon)_

## Contributing
In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [grunt](https://github.com/gruntjs/grunt).

## Release History

`0.1.0` 2012-12-06 First release.

## License
Copyright (c) 2012 PerfectWorks  
Licensed under the MIT license.
