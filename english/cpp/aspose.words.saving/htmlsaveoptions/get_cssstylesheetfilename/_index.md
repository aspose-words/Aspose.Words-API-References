---
title: Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method
linktitle: get_CssStyleSheetFileName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method. Specifies the path and the name of the Cascading Style Sheet (CSS) file written when a document is exported to HTML. Default is an empty string in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


Specifies the path and the name of the Cascading [Style](../../../aspose.words/style/) Sheet (CSS) file written when a document is exported to HTML. Default is an empty string.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## Remarks


This property has effect only when saving a document to HTML format and external CSS style sheet is requested using [CssStyleSheetType](../get_cssstylesheettype/).

If this property is empty, the CSS file will be saved into the same folder and with the same name as the HTML document but with the ".css" extension.

If only path but no file name is specified in this property, the CSS file will be saved into the specified folder and will have the same name as the HTML document but with the ".css" extension.

If the folder specified by this property doesn't exist, it will be created automatically before the CSS file is saved.

Another way to specify a folder where external CSS file is saved is to use [ResourceFolder](../get_resourcefolder/).

## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
