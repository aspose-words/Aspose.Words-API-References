---
title: FontSavingArgs.font_file_name property
linktitle: font_file_name property
articleTitle: font_file_name property
second_title: Aspose.Words for Python
description: "FontSavingArgs.font_file_name property. Gets or sets the file name (without path) where the font will be saved to."
type: docs
weight: 40
url: /python-net/aspose.words.saving/fontsavingargs/font_file_name/
---

## FontSavingArgs.font_file_name property

Gets or sets the file name (without path) where the font will be saved to.


```python
@property
def font_file_name(self) -> str:
    ...

@font_file_name.setter
def font_file_name(self, value: str):
    ...

```

### Remarks

This property allows you to redefine how the font file names are generated
during export to HTML.

When the event is fired, this property contains the file name that was generated 
by Aspose.Words. You can change the value of this property to save the font into a 
different file. Note that file names must be unique.

Aspose.Words automatically generates a unique file name for every embedded font when 
exporting to HTML format. How the font file name is generated 
depends on whether you save the document to a file or to a stream.

When saving a document to a file, the generated font file name looks like 
*\<document base file name\>.\<original file name\>\<optional suffix\>.\<extension\>*.

When saving a document to a stream, the generated font file name looks like 
*Aspose.Words.\<document guid\>.\<original file name\>\<optional suffix\>.\<extension\>*.

[FontSavingArgs.font_file_name](./) must contain only the file name without the path.
Aspose.Words determines the path for saving using the document file name, 
the [HtmlSaveOptions.fonts_folder](../../htmlsaveoptions/fonts_folder/) and
[HtmlSaveOptions.fonts_folder_alias](../../htmlsaveoptions/fonts_folder_alias/) properties.




### See Also

* module [aspose.words.saving](../../)
* class [FontSavingArgs](../)
* property [FontSavingArgs.font_stream](../font_stream/)
* property [HtmlSaveOptions.fonts_folder](../../htmlsaveoptions/fonts_folder/)
* property [HtmlSaveOptions.fonts_folder_alias](../../htmlsaveoptions/fonts_folder_alias/)

