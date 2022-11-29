---
title: get_ResolveFontNames
second_title: Aspose.Words for C++ API Reference
description: Specifies whether font family names used in the document are resolved and substituted according to FontSettings when being written into HTML-based formats.
type: docs
weight: 521
url: /cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


Specifies whether font family names used in the document are resolved and substituted according to [FontSettings](../../../aspose.words/document/get_fontsettings/) when being written into HTML-based formats.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## Remarks


By default, this option is set to **false** and font family names are written to HTML as specified in source documents. That is, [FontSettings](../../../aspose.words/document/get_fontsettings/) are ignored and no resolution or substitution of font family names is performed.

If this option is set to **true**, Aspose.Words uses [FontSettings](../../../aspose.words/document/get_fontsettings/) to resolve each font family name specified in a source document into the name of an available font family, performing font substitution as required. 
## See Also

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
