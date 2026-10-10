---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins Methode"
linktitle: "get_PageMargins"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins Methode. Gibt die Ränder um die Seiten in einem HTML-Dokument an. Der Randwert wird in Punkten gemessen und muss größer oder gleich 0 sein. Standardwert ist 10 Punkte in C++."
type: docs
weight: 13000
url: /de/cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagemargins/
---
## HtmlFixedSaveOptions::get_PageMargins method


Gibt die Ränder um die Seiten in einem HTML-Dokument an. Der Randwert wird in Punkten gemessen und muss größer oder gleich 0 sein. Standardwert ist 10 Punkte.

```cpp
double Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins() const
```

## Hinweise


Hängt vom Wert der [PageHorizontalAlignment](../get_pagehorizontalalignment/) Eigenschaft ab:

* Defines top, bottom and left page margins if the value is [Left](../../htmlfixedpagehorizontalalignment/).
* Defines top, bottom and right page margins if the value is [Right](../../htmlfixedpagehorizontalalignment/).
* Defines top and bottom page margins if the value is [Center](../../htmlfixedpagehorizontalalignment/).



## Beispiele



Zeigt, wie man Seitenränder beim Speichern eines Dokuments als HTML anpasst.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_PageMargins(15);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins/styles.css");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }")->get_Success());
```

## Siehe auch

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
