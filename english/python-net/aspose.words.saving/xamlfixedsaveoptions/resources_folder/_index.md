---
title: XamlFixedSaveOptions.resources_folder property
linktitle: resources_folder property
articleTitle: resources_folder property
second_title: Aspose.Words for Python
description: "XamlFixedSaveOptions.resources_folder property. Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format"
type: docs
weight: 30
url: /python-net/aspose.words.saving/xamlfixedsaveoptions/resources_folder/
---

## XamlFixedSaveOptions.resources_folder property

Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format.
Default is ``None``.



```python
@property
def resources_folder(self) -> str:
    ...

@resources_folder.setter
def resources_folder(self, value: str):
    ...

```

### Remarks

When you save a [Document](../../../aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all
images embedded in the document as standalone files. [XamlFixedSaveOptions.resources_folder](./)
allows you to specify where the images will be saved and [XamlFixedSaveOptions.resources_folder_alias](../resources_folder_alias/)
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the
images in the same folder where the document file is saved. Use [XamlFixedSaveOptions.resources_folder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images,
but still needs to save the images somewhere. In this case, you need to specify an accessible folder
by using the [XamlFixedSaveOptions.resources_folder](./) property




### See Also

* module [aspose.words.saving](../../)
* class [XamlFixedSaveOptions](../)
* property [XamlFixedSaveOptions.resources_folder_alias](../resources_folder_alias/)

