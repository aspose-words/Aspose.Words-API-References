---
title: Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins method
linktitle: get_PageMargins
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins method. Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagemargins/
---
## HtmlFixedSaveOptions::get_PageMargins method


Specifies the margins around pages in an HTML document. The margins value is measured in points and should be equal to or greater than 0. Default value is 10 points.

```cpp
double Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins() const
```

## Remarks


Depends on the value of [PageHorizontalAlignment](../get_pagehorizontalalignment/) property:

* Defines top, bottom and left page margins if the value is [Left](../../htmlfixedpagehorizontalalignment/).
* Defines top, bottom and right page margins if the value is [Right](../../htmlfixedpagehorizontalalignment/).
* Defines top and bottom page margins if the value is [Center](../../htmlfixedpagehorizontalalignment/).



## Examples



Shows how to adjust page margins when saving a document to HTML. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_PageMargins(15);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins/styles.css");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }")->get_Success());
```

## See Also

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
