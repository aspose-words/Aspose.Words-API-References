---
title: HtmlFixedSaveOptions.resources_folder property
linktitle: resources_folder property
articleTitle: resources_folder property
second_title: Aspose.Words for Python
description: "HtmlFixedSaveOptions.resources_folder property. Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format"
type: docs
weight: 140
url: /python-net/aspose.words.saving/htmlfixedsaveoptions/resources_folder/
---

## HtmlFixedSaveOptions.resources_folder property

Specifies the physical folder where resources (images, fonts, css) are saved when exporting a document to Html format.
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

Has effect only if [HtmlFixedSaveOptions.export_embedded_images](../export_embedded_images/) property is ``False``.

When you save a [Document](../../../aspose.words/document/) in Html format, Aspose.Words needs to save all
images embedded in the document as standalone files. [HtmlFixedSaveOptions.resources_folder](./)
allows you to specify where the images will be saved and [HtmlFixedSaveOptions.resources_folder_alias](../resources_folder_alias/)
allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the
images in the same folder where the document file is saved. Use [HtmlFixedSaveOptions.resources_folder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images,
but still needs to save the images somewhere. In this case, you need to specify an accessible folder
by using the [HtmlFixedSaveOptions.resources_folder](./) property




### See Also

* module [aspose.words.saving](../../)
* class [HtmlFixedSaveOptions](../)
* property [HtmlFixedSaveOptions.resources_folder_alias](../resources_folder_alias/)

