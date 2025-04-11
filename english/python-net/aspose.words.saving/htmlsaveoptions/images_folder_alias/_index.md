---
title: HtmlSaveOptions.images_folder_alias property
linktitle: images_folder_alias property
articleTitle: images_folder_alias property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.images_folder_alias property. Specifies the name of the folder used to construct image URIs written into an HTML document"
type: docs
weight: 370
url: /python-net/aspose.words.saving/htmlsaveoptions/images_folder_alias/
---

## HtmlSaveOptions.images_folder_alias property

Specifies the name of the folder used to construct image URIs written into an HTML document.
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

When you save a [Document](../../../aspose.words/document/) in HTML format, Aspose.Words needs to save all
images embedded in the document as standalone files. [HtmlSaveOptions.images_folder](../images_folder/)
allows you to specify where the images will be saved and [HtmlSaveOptions.images_folder_alias](./)
allows to specify how the image URIs will be constructed.

If [HtmlSaveOptions.images_folder_alias](./) is not an empty string, then the image URI written
to HTML will be *ImagesFolderAlias + \<image file name\>*.

If [HtmlSaveOptions.images_folder_alias](./) is an empty string, then the image URI written
to HTML will be *ImagesFolder + \<image file name\>*.

If [HtmlSaveOptions.images_folder_alias](./) is set to '.' (dot), then the image file name
will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct image URIs
is to use [HtmlSaveOptions.resource_folder_alias](../resource_folder_alias/).




### Examples

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
options = aw.saving.HtmlSaveOptions()
options.css_style_sheet_type = aw.saving.CssStyleSheetType.EXTERNAL
options.export_font_resources = True
options.image_resolution = 72
options.font_resources_subsetting_size_threshold = 0
options.fonts_folder = ARTIFACTS_DIR + 'Fonts'
options.images_folder = ARTIFACTS_DIR + 'Images'
options.resource_folder = ARTIFACTS_DIR + 'Resources'
options.fonts_folder_alias = 'http://example.com/fonts'
options.images_folder_alias = 'http://example.com/images'
options.resource_folder_alias = 'http://example.com/resources'
options.export_original_url_for_linked_images = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.FolderAlias.html', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.resource_folder_alias](../resource_folder_alias/)
* property [HtmlSaveOptions.images_folder](../images_folder/)
* property [HtmlSaveOptions.image_saving_callback](../image_saving_callback/)

