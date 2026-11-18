---
title: Aspose::Words::Saving::HtmlSaveOptions::set_ResolveFontNames method
linktitle: set_ResolveFontNames
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlSaveOptions::set_ResolveFontNames method. Specifies whether font family names used in the document are resolved and substituted according to FontSettings when being written into HTML-based formats in C++.'
type: docs
weight: 89000
url: /cpp/aspose.words.saving/htmlsaveoptions/set_resolvefontnames/
---
## HtmlSaveOptions::set_ResolveFontNames method


Specifies whether font family names used in the document are resolved and substituted according to [FontSettings](../../../aspose.words/document/get_fontsettings/) when being written into HTML-based formats.

```cpp
void Aspose::Words::Saving::HtmlSaveOptions::set_ResolveFontNames(bool value)
```

## Remarks


By default, this option is set to **false** and font family names are written to HTML as specified in source documents. That is, [FontSettings](../../../aspose.words/document/get_fontsettings/) are ignored and no resolution or substitution of font family names is performed.

If this option is set to **true**, Aspose.Words uses [FontSettings](../../../aspose.words/document/get_fontsettings/) to resolve each font family name specified in a source document into the name of an available font family, performing font substitution as required.
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
