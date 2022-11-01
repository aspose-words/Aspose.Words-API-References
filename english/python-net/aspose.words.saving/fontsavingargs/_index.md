---
title: FontSavingArgs class
second_title: Aspose.Words for Python via .NET API Reference
description: "Provides data for the [IFontSavingCallback.font_saving()](../ifontsavingcallback/font_saving/#fontsavingargs) event"
type: docs
weight: 190
url: /python-net/aspose.words.saving/fontsavingargs/
---

## FontSavingArgs class

Provides data for the [IFontSavingCallback.font_saving()](../ifontsavingcallback/font_saving/#fontsavingargs) event.
To learn more, visit the [Save a Document](https://docs.aspose.com/words/net/save-a-document/) documentation article.




When Aspose.Words saves a document to HTML or related formats and [HtmlSaveOptions.export_font_resources](../htmlsaveoptions/export_font_resources/) 
is set to ``True``, it saves each font subject for export into a separate file.

[FontSavingArgs](./) controls whether particular font resource should be exported and how.

[FontSavingArgs](./) also allows to redefine how font file names are generated or to 
completely circumvent saving of fonts into files by providing your own stream objects.

To decide whether to save a particular font resource, use the [FontSavingArgs.is_export_needed](./is_export_needed/) property.

To save fonts into streams instead of files, use the [FontSavingArgs.font_stream](./font_stream/) property.




### Properties

| Name | Description |
| --- | --- |
| [bold](./bold/) | Indicates whether the current font is bold. |
| [document](./document/) | Gets the document object that is being saved. |
| [font_family_name](./font_family_name/) | Indicates the current font family name. |
| [font_file_name](./font_file_name/) | Gets or sets the file name (without path) where the font will be saved to. |
| [font_stream](./font_stream/) | Allows to specify the stream where the font will be saved to. |
| [is_export_needed](./is_export_needed/) | Allows to specify whether the current font will be exported as a font resource. Default is ``True``. |
| [is_subsetting_needed](./is_subsetting_needed/) | Allows to specify whether the current font will be subsetted before exporting as a font resource. |
| [italic](./italic/) | Indicates whether the current font is italic. |
| [keep_font_stream_open](./keep_font_stream_open/) | Specifies whether Aspose.Words should keep the stream open or close it after saving a font. |
| [original_file_name](./original_file_name/) | Gets the original font file name with an extension. |
| [original_file_size](./original_file_size/) | Gets the original font file size. |

### See Also

* module [aspose.words.saving](../)

