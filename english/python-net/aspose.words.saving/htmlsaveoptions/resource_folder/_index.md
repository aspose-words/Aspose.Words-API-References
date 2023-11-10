---
title: HtmlSaveOptions.resource_folder property
linktitle: resource_folder property
articleTitle: resource_folder property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.resource_folder property. Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document is exported to HTML"
type: docs
weight: 420
url: /python-net/aspose.words.saving/htmlsaveoptions/resource_folder/
---

## HtmlSaveOptions.resource_folder property

Specifies a physical folder where all resources like images, fonts, and external CSS are saved when a document
is exported to HTML. Default is an empty string.


```python
@property
def resource_folder(self) -> str:
    ...

@resource_folder.setter
def resource_folder(self, value: str):
    ...

```

### Remarks

[HtmlSaveOptions.resource_folder](./) is the simplest way to specify a folder where all resources should be written.
Another way is to use individual properties [HtmlSaveOptions.fonts_folder](../fonts_folder/), [HtmlSaveOptions.images_folder](../images_folder/),
and [HtmlSaveOptions.css_style_sheet_file_name](../css_style_sheet_file_name/).

[HtmlSaveOptions.resource_folder](./) has a lower priority than folders specified via [HtmlSaveOptions.fonts_folder](../fonts_folder/),
[HtmlSaveOptions.images_folder](../images_folder/), and [HtmlSaveOptions.css_style_sheet_file_name](../css_style_sheet_file_name/). For example, if both
[HtmlSaveOptions.resource_folder](./) and [HtmlSaveOptions.fonts_folder](../fonts_folder/) are specified, fonts will be saved
to [HtmlSaveOptions.fonts_folder](../fonts_folder/), while images and CSS will be saved to [HtmlSaveOptions.resource_folder](./).

If the folder specified by [HtmlSaveOptions.resource_folder](./) doesn't exist, it will be created automatically.





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
* property [HtmlSaveOptions.fonts_folder](../fonts_folder/)
* property [HtmlSaveOptions.images_folder](../images_folder/)
* property [HtmlSaveOptions.css_style_sheet_file_name](../css_style_sheet_file_name/)

