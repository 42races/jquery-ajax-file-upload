# jQuery Ajax File Upload

## usage


Load the script files first. In html page create a target element.

     <div class="uploader"></div>

Add the following code in your javascript

     $(".uploader").ajaxUpload({
        callback: function(data) {
          // data containes json response from server
        }
     });

# Options supported

    upload_path: "/"              // to which the file is uploaded POST request
    browse_text: "browse"         // text on the browse link
    multiple: true                // choose multiple files


Ajax upload comes with a simple scss (css) file you are free to override the default styling.
A new li is added for each selected file. The DOM structure created by the plugin is as follows

    <div class="uploader upload">
         <a href="javascript:void(0);" class="browse">browse</a>
         <input type="file" hidden="" multiple="true">
         <ul class="list">
             <li>
                <div class="progressbar"><div class="progress" style="width: 100%;"></div></div>
                <div class="filemeta">
                     <div class="filename">559044_472813522756703_1821444898_n.jpg</div>
                     <div class="fileinfo"><span>69 KB</span>&nbsp;—&nbsp;<a id="12121" class="delete-link" data-path="/profile_photo/12121" href="javascript:void(0);">delete</a></div>
                </div>
             </li>
         </ul>
    </div>



eg:

    <html>
        <head>
            <title>Ajax Multi File Upload Plugin</title>
            <link rel="stylesheet" type="text/css" href="jquery_ajax_upload/style.css" />
            <script type="text/javascript" src="jquery_ajax_upload/jquery2.min.js"></script>
            <script type="text/javascript" src="jquery_ajax_upload/jquery.ajaxupload.js"></script>
            <script>
                $(function(){
                    $(".uploader").ajaxUpload();
                });
            </script>
        </head>
        <body>
            <div class="uploader"></div>
        </body>
    </html>