---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins method"
linktitle: "get_PageMargins"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins method. Anger marginalerna runt sidor i ett HTML-dokument. Marginalvärdet mäts i punkter och ska vara lika med eller större än 0. Standardvärdet är 10 punkter i C++."
type: docs
weight: 13000
url: /sv/cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagemargins/
---
## HtmlFixedSaveOptions::get_PageMargins method


Anger marginalerna runt sidor i ett HTML-dokument. Marginalvärdet mäts i punkter och bör vara lika med eller större än 0. Standardvärdet är 10 punkter.

```cpp
double Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins() const
```

## Anmärkningar


Beror på värdet av egenskapen [PageHorizontalAlignment](../get_pagehorizontalalignment/):

* Defines top, bottom and left page margins if the value is [Left](../../htmlfixedpagehorizontalalignment/).
* Defines top, bottom and right page margins if the value is [Right](../../htmlfixedpagehorizontalalignment/).
* Defines top and bottom page margins if the value is [Center](../../htmlfixedpagehorizontalalignment/).



## Exempel



Visar hur man justerar sidmarginaler när ett dokument sparas till HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_PageMargins(15);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins/styles.css");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }")->get_Success());
```

## Se även

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
