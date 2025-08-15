---
title: XamlFlowSaveOptions.images_folder property
linktitle: images_folder property
articleTitle: images_folder property
second_title: Aspose.Words for Python
description: "XamlFlowSaveOptions.images_folder property. Specifies the physical folder where images are saved when exporting a document to XAML format"
type: docs
weight: 30
url: /python-net/aspose.words.saving/xamlflowsaveoptions/images_folder/
---

## XamlFlowSaveOptions.images_folder property

Specifies the physical folder where images are saved when exporting a document to XAML format.
Default is an empty string.


```python
@property
def images_folder(self) -> str:
    ...

@images_folder.setter
def images_folder(self, value: str):
    ...

```

### Remarks

When you save a [Document](../../../aspose.words/document/) in XAML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [XamlFlowSaveOptions.images_folder](./) 
allows you to specify where the images will be saved and [XamlFlowSaveOptions.images_folder_alias](../images_folder_alias/) 
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the 
images in the same folder where the document file is saved. Use [XamlFlowSaveOptions.images_folder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, 
but still needs to save the images somewhere. In this case, you need to specify an accessible folder 
in the [XamlFlowSaveOptions.images_folder](./) property or provide custom streams via 
the [XamlFlowSaveOptions.image_saving_callback](../image_saving_callback/) event handler.




### See Also

* module [aspose.words.saving](../../)
* class [XamlFlowSaveOptions](../)
* property [XamlFlowSaveOptions.images_folder_alias](../images_folder_alias/)
* property [XamlFlowSaveOptions.image_saving_callback](../image_saving_callback/)

