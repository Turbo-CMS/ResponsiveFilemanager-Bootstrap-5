# Responsive FileManager Bootstrap 5 for TinyMCE

PRODUCTION VERSION DOWNLOAD: https://github.com/Turbo-CMS/ResponsiveFilemanager-Bootstrap-5/releases

Released under Creative Commons Attribution-NonCommercial 3.0 Unported License.

### Server Requirements

- PHP 7.1 or above strongly recommended
- [Apache 2.2 or 2.4](https://httpd.apache.org/)

### Use as TinyMCE 7 File Manager

Copy tinymce/plugins/responsivefilemanager folder to tinymce/plugins/ in your server
N.B.: REMEMBER THAT RESPONVIVEFILEMANAGER IS NOT FILEMANAGER FOLDER BUT AN ADDITIONAL PLUGIN
Settings of tinymce should be like this: (remember to add responsivefilemanager in plugins list)

```js
   tinymce.init({
      selector: 'textarea',
      height: 500,
      plugins: [
         'advlist', 'autolink', 'lists', 'link', 'image', 'charmap', 'preview',
         'anchor', 'searchreplace', 'visualblocks', 'code', 'fullscreen',
         'insertdatetime', 'media', 'table', 'help', 'wordcount'
      ],
      toolbar: 'undo redo | blocks | ' +
      'bold italic backcolor | alignleft aligncenter ' +
      'alignright alignjustify | bullist numlist outdent indent | ' +
      'removeformat | media image | help',
      content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:16px }',
      external_filemanager_path:"/filemanager/",
      filemanager_title:"Responsive Filemanager" ,
      external_plugins: { "filemanager" : "/filemanager/plugin.min.js"}
      });
   ```

You can pass this variables on TinyMCE init.
filemanager_title the title of filemanager window default="Responsive filemanager"
filemanager_sort_by: the element to sorting (values: name,size,extension,date) default=""
filemanager_descending: descending ? or ascending (values=1 or 0) default="0"

> [!WARNING]
> If you want full path url in tinyMCE paths you can add relative_urls: false on tinyMCE init
> external_filemanager_path and external_plugins path must be absolute from root and must point to filemanager folder not responsivefilemanager plugin folder

Change the path in your tinymce init function in external_filemanager_path and external_plugins (the path must be a absolute path from base_url of your site and must start with / so in this example i have the filemanager folder in www.site.com/filemanager/)

> [!WARNING]
> If you are updating from older version (from 1 to 7) substitute your tinyMCE with new or download only the image/media/link originals folders and copy in your tinyMCE plugin folder   

### Dark Mode

```js
   tinymce.init({
      selector: 'textarea',
      skin: "oxide-dark",
      content_css: "dark",
      height: 500,
      plugins: [
         'advlist', 'autolink', 'lists', 'link', 'image', 'charmap', 'preview',
         'anchor', 'searchreplace', 'visualblocks', 'code', 'fullscreen',
         'insertdatetime', 'media', 'table', 'help', 'wordcount'
      ],
      toolbar: 'undo redo | blocks | ' +
      'bold italic backcolor | alignleft aligncenter ' +
      'alignright alignjustify | bullist numlist outdent indent | ' +
      'removeformat | media image | help',
      content_style: 'body { font-family:Helvetica,Arial,sans-serif; font-size:16px }',
      external_filemanager_path:"/filemanager/",
      filemanager_title:"Responsive Filemanager" ,
      external_plugins: { "filemanager" : "/filemanager/plugin.min.js"}
      });
   ```