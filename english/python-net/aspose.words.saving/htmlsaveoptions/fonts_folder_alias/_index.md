---
title: HtmlSaveOptions.fonts_folder_alias property
linktitle: fonts_folder_alias property
articleTitle: fonts_folder_alias property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.fonts_folder_alias property. Specifies the name of the folder used to construct font URIs written into an HTML document"
type: docs
weight: 320
url: /python-net/aspose.words.saving/htmlsaveoptions/fonts_folder_alias/
---

## HtmlSaveOptions.fonts_folder_alias property

Specifies the name of the folder used to construct font URIs written into an HTML document.
Default is an empty string.


```python
@property
def fonts_folder_alias(self) -> str:
    ...

@fonts_folder_alias.setter
def fonts_folder_alias(self, value: str):
    ...

```

### Remarks

When you save a [Document](../../../aspose.words/document/) in HTML format and [HtmlSaveOptions.export_font_resources](../export_font_resources/) 
is set to ``True``, Aspose.Words needs to save fonts used in the document as standalone files. 
[HtmlSaveOptions.fonts_folder](../fonts_folder/) allows you to specify where the fonts will be saved and 
[HtmlSaveOptions.fonts_folder_alias](./) allows to specify how the font URIs will be constructed.

If [HtmlSaveOptions.fonts_folder_alias](./) is not an empty string, then the font URI written
to HTML will be *FontsFolderAlias + \<font file name\>*.

If [HtmlSaveOptions.fonts_folder_alias](./) is an empty string, then the font URI written 
to HTML will be *FontsFolder + \<font file name\>*.

If [HtmlSaveOptions.fonts_folder_alias](./) is set to '.' (dot), then the font file name 
will be written to HTML without path regardless of other options.

Alternative way to specify the name of the folder to construct font URIs
is to use [HtmlSaveOptions.resource_folder_alias](../resource_folder_alias/).




### Examples

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```python
doc = aw.Document(MY_DIR + "Rendering.docx")

options = aw.saving.HtmlSaveOptions()
options.css_style_sheet_type = aw.saving.CssStyleSheetType.EXTERNAL
options.export_font_resources = True
options.image_resolution = 72
options.font_resources_subsetting_size_threshold = 0
options.fonts_folder = ARTIFACTS_DIR + "Fonts"
options.images_folder = ARTIFACTS_DIR + "Images"
options.resource_folder = ARTIFACTS_DIR + "Resources"
options.fonts_folder_alias = "http://example.com/fonts"
options.images_folder_alias = "http://example.com/images"
options.resource_folder_alias = "http://example.com/resources"
options.export_original_url_for_linked_images = True

doc.save(ARTIFACTS_DIR + "HtmlSaveOptions.folder_alias.html", options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.resource_folder_alias](../resource_folder_alias/)
* property [HtmlSaveOptions.export_font_resources](../export_font_resources/)
* property [HtmlSaveOptions.fonts_folder](../fonts_folder/)
* property [HtmlSaveOptions.font_saving_callback](../font_saving_callback/)

