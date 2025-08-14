---
title: XamlFlowSaveOptions.images_folder_alias property
linktitle: images_folder_alias property
articleTitle: images_folder_alias property
second_title: Aspose.Words for Python
description: "XamlFlowSaveOptions.images_folder_alias property. Specifies the name of the folder used to construct image URIs written into an XAML document"
type: docs
weight: 40
url: /python-net/aspose.words.saving/xamlflowsaveoptions/images_folder_alias/
---

## XamlFlowSaveOptions.images_folder_alias property

Specifies the name of the folder used to construct image URIs written into an XAML document.
Default is an empty string.


```python
@property
def images_folder_alias(self) -> str:
    ...

@images_folder_alias.setter
def images_folder_alias(self, value: str):
    ...

```

### Remarks

When you save a [Document](../../../aspose.words/document/) in XAML format, Aspose.Words needs to save all 
images embedded in the document as standalone files. [XamlFlowSaveOptions.images_folder](../images_folder/) 
allows you to specify where the images will be saved and [XamlFlowSaveOptions.images_folder_alias](./) 
allows to specify how the image URIs will be constructed.

If [XamlFlowSaveOptions.images_folder_alias](./) is not an empty string, then the image URI written
to XAML will be *ImagesFolderAlias + \<image file name\>*.

If [XamlFlowSaveOptions.images_folder_alias](./) is an empty string, then the image URI written 
to XAML will be *ImagesFolder + \<image file name\>*.

If [XamlFlowSaveOptions.images_folder_alias](./) is set to '.' (dot), then the image file name 
will be written to XAML without path regardless of other options.




### See Also

* module [aspose.words.saving](../../)
* class [XamlFlowSaveOptions](../)
* property [XamlFlowSaveOptions.images_folder](../images_folder/)
* property [XamlFlowSaveOptions.image_saving_callback](../image_saving_callback/)

