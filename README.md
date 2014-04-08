# grunt-fontface

> Generate CSS/SCSS from all font files within a font directory

## Getting Started
This plugin requires Grunt `~0.4.4`

If you haven't used [Grunt](http://gruntjs.com/) before, be sure to check out the [Getting Started](http://gruntjs.com/getting-started) guide, as it explains how to create a [Gruntfile](http://gruntjs.com/sample-gruntfile) as well as install and use Grunt plugins. Once you're familiar with that process, you may install this plugin with this command:

```shell
npm install grunt-fontface --save-dev
```

Once the plugin has been installed, it may be enabled inside your Gruntfile with this line of JavaScript:

```js
grunt.loadNpmTasks('grunt-fontface');
```

## The "fontface" task

### Overview
In your project's Gruntfile, add a section named `fontface` to the data object passed into `grunt.initConfig()`.

```js
grunt.initConfig({
  fontface: {
    dist: {
      options: {
      fontDir: 'fonts'
      template: "@font-face {" +
                      "font-family: 'MyFontFamily';" +
                      "src: url('{{font}}.eot?#iefix') format('embedded-opentype')," +
                      "url('{{font}}.woff') format('woff')," +
                      "url('{{font}}.ttf')  format('truetype')," +
                      "url('{{font}}.svg#{{font}}') format('svg');" +
                    "}"
      }
    }
    
  },
});
```

### Options

#### options.template
Type: `String`
Default value: none
Required: true

String that will be output for each font. Uses handlebars style template interpolation `{{ font }}`.
 Example:

	"@font-face {" +
		"font-family: 'MyFontFamily';" +
		"src: url('{{font}}.eot?#iefix') format('embedded-opentype')," +
		"url('{{font}}.woff') format('woff')," +
		"url('{{font}}.ttf')  format('truetype')," +
		"url('{{font}}.svg#{{font}}') format('svg');" +
	"}"

#### options.fontDir
Type: `String`
Default value: 'fonts'

Location of the fonts directory

### options.outputFile

Type: `String`
Default value: 'sass/_fonts.scss'

Location of the output css/scss

### options.removeFromFile

Type: `String`
Default value: '-webfont'

Removes string from filename. 

## Release History
v 0.8.0 It's working!
