# file-reader
`<file-reader>` is a graphical element that upload a file, via button or drag&drop, and read it as a text-file when asked to.

Example:

    <file-reader id="filereaderElem"></file-reader>
    <script>
      (function() {
        var reader = document.getElementById('filereaderElem');
        reader.returnFunction = function(){
          var callback = {
            onload: function(e){ console.log(e.target.result); },
            onprogress: function(){},
            onerror: function(){}  
          }  
          reader.getSample(0,callback);
        }
      })();
    <script>  
 
