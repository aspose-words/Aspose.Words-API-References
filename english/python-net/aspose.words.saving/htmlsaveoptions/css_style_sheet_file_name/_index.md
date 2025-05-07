---
title: HtmlSaveOptions.css_style_sheet_file_name property
linktitle: css_style_sheet_file_name property
articleTitle: css_style_sheet_file_name property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.css_style_sheet_file_name property. Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML"
type: docs
weight: 50
url: /python-net/aspose.words.saving/htmlsaveoptions/css_style_sheet_file_name/
---

## HtmlSaveOptions.css_style_sheet_file_name property

Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document
is exported to HTML.
Default is an empty string.


```python
@property
def css_style_sheet_file_name(self) -> str:
    ...

@css_style_sheet_file_name.setter
def css_style_sheet_file_name(self, value: str):
    ...

```

### Remarks

This property has effect only when saving a document to HTML format
and external CSS style sheet is requested using [HtmlSaveOptions.css_style_sheet_type](../css_style_sheet_type/).

If this property is empty, the CSS file will be saved into the same folder and with the same name as the HTML
document but with the ".css" extension.

If only path but no file name is specified in this property, the CSS file will be saved into the specified
folder and will have the same name as the HTML document but with the ".css" extension.

If the folder specified by this property doesn't exist, it will be created automatically before the CSS file
is saved.

Another way to specify a folder where external CSS file is saved is to use [HtmlSaveOptions.resource_folder](../resource_folder/).





### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.resource_folder](../resource_folder/)
* property [HtmlSaveOptions.resource_folder_alias](../resource_folder_alias/)
* property [HtmlSaveOptions.css_style_sheet_type](../css_style_sheet_type/)

