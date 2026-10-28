---
title: Aspose::Words::Saving::HtmlSaveOptions::set_ExportFontResources method
linktitle: set_ExportFontResources
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::set_ExportFontResources method. Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is false in C++.'
type: docs
weight: 63000
url: /cpp/aspose.words.saving/htmlsaveoptions/set_exportfontresources/
---
## HtmlSaveOptions::set_ExportFontResources method


Specifies whether font resources should be exported to HTML, MHTML or EPUB. Default is **false**.

```cpp
void Aspose::Words::Saving::HtmlSaveOptions::set_ExportFontResources(bool value)
```

## Remarks


Exporting font resources allows for consistent document rendering independent of the fonts available in a given user's environment.

If [ExportFontResources](../get_exportfontresources/) is set to **true**, main HTML document will refer to every font via the CSS 3 @font-face at-rule and fonts will be output as separate files. When exporting to IDPF EPUB or MHTML formats, fonts will be embedded into the corresponding package along with other subsidiary files.

If [ExportFontsAsBase64](../get_exportfontsasbase64/) is set to **true**, fonts will not be saved to separate files. Instead, they will be embedded into @font-face at-rules in Base64 encoding.

 Important! When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. License agreements that cover some fonts specifically note that usage via @font-face rules in CSS style sheets is not allowed. Font subsetting can also violate license terms. 
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
