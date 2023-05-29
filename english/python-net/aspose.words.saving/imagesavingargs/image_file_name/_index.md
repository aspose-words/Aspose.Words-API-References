---
title: ImageSavingArgs.image_file_name property
linktitle: image_file_name property
articleTitle: image_file_name property
second_title: Aspose.Words for Python
description: "ImageSavingArgs.image_file_name property. Gets or sets the file name (without path) where the image will be saved to."
type: docs
weight: 30
url: /python-net/aspose.words.saving/imagesavingargs/image_file_name/
---

## ImageSavingArgs.image_file_name property

Gets or sets the file name (without path) where the image will be saved to.

This property allows you to redefine how the image file names are generated
during export to HTML.

When the event is fired, this property contains the file name that was generated 
by Aspose.Words. You can change the value of this property to save the image into a 
different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded image when 
exporting to HTML format. How the image file name is generated 
depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated image file name looks like 
*\<document base file name\>.\<image number\>.\<extension\>*.

When saving a document to a stream, the generated image file name looks like 
*Aspose.Words.\<document guid\>.\<image number\>.\<extension\>*.

[ImageSavingArgs.image_file_name](./) must contain only the file name without the path.
Aspose.Words determines the path for saving and the value of the ``src`` attribute for writing 
to HTML using the document file name, the [HtmlSaveOptions.images_folder](../../htmlsaveoptions/images_folder/) and
[HtmlSaveOptions.images_folder_alias](../../htmlsaveoptions/images_folder_alias/) properties.




### See Also

* module [aspose.words.saving](../../)
* class [ImageSavingArgs](../)
* property [ImageSavingArgs.current_shape](../current_shape/)
* property [ImageSavingArgs.is_image_available](../is_image_available/)
* property [ImageSavingArgs.image_stream](../image_stream/)
* property [HtmlSaveOptions.images_folder](../../htmlsaveoptions/images_folder/)
* property [HtmlSaveOptions.images_folder_alias](../../htmlsaveoptions/images_folder_alias/)

