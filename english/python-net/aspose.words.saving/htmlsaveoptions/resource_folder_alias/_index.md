---
title: HtmlSaveOptions.resource_folder_alias property
linktitle: resource_folder_alias property
articleTitle: resource_folder_alias property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.resource_folder_alias property. Specifies the name of the folder used to construct URIs of all resources written into an HTML document"
type: docs
weight: 450
url: /python-net/aspose.words.saving/htmlsaveoptions/resource_folder_alias/
---

## HtmlSaveOptions.resource_folder_alias property

Specifies the name of the folder used to construct URIs of all resources written into an HTML document.
Default is an empty string.


```python
@property
def resource_folder_alias(self) -> str:
    ...

@resource_folder_alias.setter
def resource_folder_alias(self, value: str):
    ...

```

### Remarks

[HtmlSaveOptions.resource_folder_alias](./) is the simplest way to specify how URIs for all resource files should be
constructed. Same information can be specified for images and fonts separately via [HtmlSaveOptions.images_folder_alias](../images_folder_alias/)
and [HtmlSaveOptions.fonts_folder_alias](../fonts_folder_alias/) properties, respectively. However, there is no individual property for CSS.


[HtmlSaveOptions.resource_folder_alias](./) has lower priority than [HtmlSaveOptions.fonts_folder_alias](../fonts_folder_alias/)
and [HtmlSaveOptions.images_folder_alias](../images_folder_alias/). For example, if both [HtmlSaveOptions.resource_folder_alias](./)
and [HtmlSaveOptions.fonts_folder_alias](../fonts_folder_alias/) are specified, fonts' URIs will be constructed using
[HtmlSaveOptions.fonts_folder_alias](../fonts_folder_alias/), while URIs of images and CSS will be constructed using
[HtmlSaveOptions.resource_folder_alias](./).

If [HtmlSaveOptions.resource_folder_alias](./) is empty, the [HtmlSaveOptions.resource_folder](../resource_folder/) property value will be used
to construct resource URIs.

If [HtmlSaveOptions.resource_folder_alias](./) is set to '.' (dot), resource URIs will contain file names only, without
any path.




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
* property [HtmlSaveOptions.resource_folder](../resource_folder/)
* property [HtmlSaveOptions.fonts_folder_alias](../fonts_folder_alias/)
* property [HtmlSaveOptions.images_folder_alias](../images_folder_alias/)

