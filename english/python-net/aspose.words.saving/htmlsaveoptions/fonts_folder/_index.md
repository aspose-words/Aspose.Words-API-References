---
title: HtmlSaveOptions.fonts_folder property
linktitle: fonts_folder property
articleTitle: fonts_folder property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.fonts_folder property. Specifies the physical folder where fonts are saved when exporting a document to HTML"
type: docs
weight: 320
url: /python-net/aspose.words.saving/htmlsaveoptions/fonts_folder/
---

## HtmlSaveOptions.fonts_folder property

Specifies the physical folder where fonts are saved when exporting a document to HTML.
Default is an empty string.

When you save a [Document](../../../aspose.words/document/) in HTML format and [HtmlSaveOptions.export_font_resources](../export_font_resources/) 
is set to ``True``, Aspose.Words needs to save fonts used in the document as standalone files. 
[HtmlSaveOptions.fonts_folder](./) allows you to specify where the fonts will be saved and 
[HtmlSaveOptions.fonts_folder_alias](../fonts_folder_alias/) allows to specify how the font URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the 
fonts in the same folder where the document file is saved. Use [HtmlSaveOptions.fonts_folder](./)
to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the fonts, 
but still needs to save the fonts somewhere. In this case, you need to specify an accessible folder 
in the [HtmlSaveOptions.fonts_folder](./) property or provide custom streams via 
the [HtmlSaveOptions.font_saving_callback](../font_saving_callback/) event handler.

If the folder specified by [HtmlSaveOptions.fonts_folder](./) doesn't exist, it will be created automatically.

[HtmlSaveOptions.resource_folder](../resource_folder/) is another way to specify a folder where fonts should be saved.




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
* property [HtmlSaveOptions.resource_folder](../resource_folder/)
* property [HtmlSaveOptions.export_font_resources](../export_font_resources/)
* property [HtmlSaveOptions.fonts_folder_alias](../fonts_folder_alias/)
* property [HtmlSaveOptions.font_saving_callback](../font_saving_callback/)

