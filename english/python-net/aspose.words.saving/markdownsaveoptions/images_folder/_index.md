---
title: MarkdownSaveOptions.images_folder property
linktitle: images_folder property
articleTitle: images_folder property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.images_folder property. Specifies the physical folder where images are saved when exporting a document to the [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format"
type: docs
weight: 70
url: /python-net/aspose.words.saving/markdownsaveoptions/images_folder/
---

## MarkdownSaveOptions.images_folder property

Specifies the physical folder where images are saved when exporting a document to
the [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format. Default is an empty string.



```python
@property
def images_folder(self) -> str:
    ...

@images_folder.setter
def images_folder(self, value: str):
    ...

```

### Remarks

When you save a [Document](../../../aspose.words/document/) in [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format,
Aspose.Words needs to save all images embedded in the document as standalone files.
[MarkdownSaveOptions.images_folder](./) allows you to specify where the images will be saved.


If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in
the same folder where the document file is saved. Use [MarkdownSaveOptions.images_folder](./) to override this behavior.


If you save a document into a stream, Aspose.Words does not have a folder
where to save the images, but still needs to save the images somewhere. In this case,
you need to specify an accessible folder in the [MarkdownSaveOptions.images_folder](./) property.


If the folder specified by [MarkdownSaveOptions.images_folder](./) doesn't exist, it will be created automatically.





### Examples

Shows how to specifies the name of the folder used to construct image URIs.

```python
builder = aw.DocumentBuilder()
builder.writeln('Some image below:')
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
saveOptions = aw.saving.MarkdownSaveOptions()
# Use the "ImagesFolder" property to assign a folder in the local file system into which
# Aspose.Words will save all the document's linked images.
saveOptions.images_folder = ARTIFACTS_DIR + 'ImagesDir/'
# Use the "ImagesFolderAlias" property to use this folder
# when constructing image URIs instead of the images folder's name.
saveOptions.images_folder_alias = 'http://example.com/images'
builder.document.save(ARTIFACTS_DIR + 'MarkdownSaveOptions.ImagesFolder.md', saveOptions)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)

