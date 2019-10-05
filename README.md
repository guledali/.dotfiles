# Visual Studio Code settings
This is my configuration for vscode.



## Installed plugins

- [File Utils](https://marketplace.visualstudio.com/items?itemName=sleistner.vscode-fileutils)
- [jumpy](https://marketplace.visualstudio.com/items?itemName=wmaurer.vscode-jumpy)
- [Create File & Folder : On The Go](https://marketplace.visualstudio.com/items?itemName=ritwickdey.create-file-folder&ssr=false)


### Ruby Intellisense and CSS
- [vscode-solargraph](https://marketplace.visualstudio.com/items?itemName=castwide.solargraph)
- [IntelliSense for CSS](https://marketplace.visualstudio.com/items?itemName=gencer.html-slim-scss-css-class-completion)
- [Simple Ruby ERB](https://marketplace.visualstudio.com/items?itemName=vortizhe.simple-ruby-erb)

#### Diagnostics (Linting)
In you workspace add remote stylesheet like   
```
"html-css-class-completion.remoteStyleSheets": [
		"https://stackpath.bootstrapcdn.com/bootstrap/3.4.1/css/bootstrap.min.css"
	]
``` 
and set it to  `"css.fileExtensions": [ "css", "scss"]`
<hr />

To enable diagnostics, set the `solargraph.diagnostics` configuration to `true`.

Solargraph uses RuboCop for diagnostics by default. If your project has a .solargraph.yml file, you can configure the diagnostics in its `reporters` section. Example:


    include:
     - "**/*.rb"
    exclude:
     - spec/**/*
     - test/**/*
     - vendor/**/*
     - ".bundle/**/*"
    require: 
     - actioncable
     - actionmailer
     - actionpack
     - actionview
     - activejob
     - activemodel
     - activerecord
     - activestorage
     - activesupport
    domains: []
    reporters:
     - typecheck
    require_paths: []
    max_files: 5000
