ok

<form action="/action_page.php">
  <input type="file" id="myFile" name="filename">
  <input type="submit">
</form>

<body>
    <input id="uploadFile" type="file" />
    <input type="button" value="rename and download" onclick="initImageUpload()" />
    <a id="aDownload">
</body>
<script>
    function initImageUpload() {
        var file = uploadFile.files[0];
        var a = document.getElementById('aDownload');
        a.href = file.name;

        var ext = file.name.split('.').pop();
        var filename = file.name.substring(0, file.name.lastIndexOf('.'));

        var newFileName = filename + "new" + "." + ext;//provide the new name here

        a.setAttribute("download", newFileName);
        a.click();
    }
</script>
</html>
