---
title: MarkdownSaveOptions.images_folder_alias property
linktitle: images_folder_alias property
articleTitle: images_folder_alias property
second_title: Aspose.Words for Python
description: "MarkdownSaveOptions.images_folder_alias property. Specifies the name of the folder used to construct image URIs written into a document"
type: docs
weight: 90
url: /zh/python-net/aspose.words.saving/markdownsaveoptions/images_folder_alias/
---

## MarkdownSaveOptions.images_folder_alias property

Specifies the name of the folder used to construct image URIs written into a document.
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

When you save a [Document](../../../aspose.words/document/) in [SaveFormat.MARKDOWN](../../../aspose.words/saveformat/#MARKDOWN) format,
Aspose.Words needs to save all images embedded in the document as standalone files.
[MarkdownSaveOptions.images_folder](../images_folder/) allows you to specify where the images will be saved and
[MarkdownSaveOptions.images_folder_alias](./) allows to specify how the image URIs will be constructed.

If [MarkdownSaveOptions.images_folder_alias](./) is not an empty string, then the image URI written
to Markdown will be *ImagesFolderAlias + \<image file name\>*.

If [MarkdownSaveOptions.images_folder_alias](./) is an empty string, then the image URI written
to Markdown will be *ImagesFolder + \<image file name\>*.

If [MarkdownSaveOptions.images_folder_alias](./) is set to '.' (dot), then the image file name
will be written to Markdown without path regardless of other options.




### Examples

Shows how to specifies the name of the folder used to construct image URIs.

```python
builder = aw.DocumentBuilder()
builder.writeln('Some image below:')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
images_folder = os.path.join(ARTIFACTS_DIR, 'ImagesDir')
save_options = aw.saving.MarkdownSaveOptions()
# 使用 "ImagesFolder" 属性指定本地文件系统中的一个文件夹，
# Aspose.Words 将把所有文档链接的图像保存到该文件夹中。
save_options.images_folder = images_folder
# 使用 "ImagesFolderAlias" 属性来使用此文件夹
# 在构建图像 URI 时，而不是使用图像文件夹的名称。
save_options.images_folder_alias = 'http://example.com/images'
builder.document.save(file_name=ARTIFACTS_DIR + 'MarkdownSaveOptions.ImagesFolder.md', save_options=save_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [MarkdownSaveOptions](../)
* property [MarkdownSaveOptions.images_folder](../images_folder/)
* property [MarkdownSaveOptions.image_saving_callback](../image_saving_callback/)

