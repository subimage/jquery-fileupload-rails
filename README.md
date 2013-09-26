# jQuery File Upload for Rails

[jQuery-File-Plugin](https://github.com/blueimp/jQuery-File-Upload) is a file upload plugin written by [Sebastian Tschan](https://github.com/blueimp). jQuery File Upload features multiple file selection, drag&drop support, progress bars and preview images for jQuery. Supports cross-domain, chunked and resumable file uploads and client-side image resizing.

jquery-fileupload-rails is a library that integrates jQuery Fule Upload for Rails 3.1 and higher.

## Plugin versions

* jQuery File Upload User Interface Plugin 8.8.5
* jQuery File Upload Plugin 5.32.6
* jQuery UI Widget 1.10.3+amd

## Installing Gem

    gem "jquery-fileupload-rails"

## Using the javascripts

Require jquery-fileupload in your app/assets/application.js file.

    //= require jquery-fileupload

The snippet above will add the following js files to the mainfest file.

    //=require jquery-fileupload/vendor/jquery.ui.widget
    //=require jquery-fileupload/vendor/load-image/load-image
    //=require jquery-fileupload/vendor/canvas-to-blob
    //=require jquery-fileupload/vendor/tmpl
    //=require jquery-fileupload/jquery.iframe-transport
    //=require jquery-fileupload/jquery.fileupload
    //=require jquery-fileupload/jquery.fileupload-ui

If you only need the basic files, just add the code below to your application.js file. [Basic setup guide](https://github.com/blueimp/jQuery-File-Upload/wiki/Basic-plugin)

    //= require jquery-fileupload/basic

The basic setup only includes the following files:

    //= require jquery-fileupload/vendor/jquery.ui.widget
    //= require jquery-fileupload/jquery.iframe-transport
    //= require jquery-fileupload/jquery.fileupload

## Using the stylesheet

Require the stylesheet file to app/assets/stylesheets/application.css

    *= require jquery.fileupload-ui

## Usign the stylesheet

Require the stylesheet file to app/assets/stylesheets/application.css

    *= require jquery.fileupload

Or, if you are using jQuery UI

    *= require jquery.fileupload-ui

## Using the load-image

You can use full version of load-image library:

    //= require jquery-fileupload/vendor/load-image

or use some parts:

    //= require ./load-image
    //= require ./load-image-orientation
    //= require ./load-image-meta
    //= require ./load-image-ios
    //= require ./load-image-exif
    //= require ./load-image-exif-map

## Using the middleware

The `jquery.iframe-transport` fallback transport has some special caveats regarding the response data type, http status, and character encodings. `jquery-fileupload-rails` includes a middleware that handles these inconsistencies seamlessly. If you decide to use it, create an initializer that adds the middleware to your application's middleware stack.

    Rails.application.config.middleware.use JQuery::FileUpload::Rails::Middleware

## [Example app](https://github.com/tors/jquery-fileupload-rails-paperclip-example)
This app uses paperclip and twitter-bootstrap-rails

You can also check out Ryan Bate's RailsCast [jQuery File Upload episode](http://railscasts.com/episodes/381-jquery-file-upload). You will
need a pro account to watch it though.


## Thanks
Thanks to [Sebastian Tschan](https://github.com/blueimp) for writing an awesome file upload plugin.

## License
Copyright (c) 2013 Tors Dalid

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
