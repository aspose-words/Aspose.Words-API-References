---
title: images_folder property
second_title: Aspose.Words for Python via .NET API Reference
description: "Specifies the physical folder where images are saved when exporting a document to HTML format"
type: docs
weight: 370
url: /python-net/aspose.words.saving/htmlsaveoptions/images_folder/
---

## HtmlSaveOptions.images_folder property

Specifies the physical folder where images are saved when exporting a document to HTML format.
Default is an empty string.

When you save a [Document](../../../aspose.words/document/) in HTML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [HtmlSaveOptions.images_folder](./) 
allows you to specify where the images will be saved and [HtmlSaveOptions.images_folder_alias](../images_folder_alias/) 
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the 
images in the same folder where the document file is saved. Use [HtmlSaveOptions.images_folder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, 
but still needs to save the images somewhere. In this case, you need to specify an accessible folder 
in the [HtmlSaveOptions.images_folder](./) property or provide custom streams via 
the [HtmlSaveOptions.image_saving_callback](../image_saving_callback/) event handler.

If the folder specified by [HtmlSaveOptions.images_folder](./) doesn't exist, it will be created automatically.

[HtmlSaveOptions.resource_folder](../resource_folder/) is another way to specify a folder where images should be saved.




### Examples

Shows how to specify the folder for storing linked images after saving to .html.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

images_dir = os.path.join(ARTIFACTS_DIR, "SaveHtmlWithOptions")

if os.path.exists(images_dir):
    shutil.rmtree(images_dir)

os.makedirs(images_dir)

# Set an option to export form fields as plain text instead of HTML input elements.
options = aw.saving.HtmlSaveOptions(aw.SaveFormat.HTML)
options.export_text_input_form_field_as_text = True
options.images_folder = images_dir

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.image_folder.html", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.resource_folder](../resource_folder/)
* property [HtmlSaveOptions.images_folder_alias](../images_folder_alias/)
* property [HtmlSaveOptions.image_saving_callback](../image_saving_callback/)

