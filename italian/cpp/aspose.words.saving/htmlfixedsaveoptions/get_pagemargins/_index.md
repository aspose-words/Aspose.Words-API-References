---
title: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins metodo"
linktitle: "get_PageMargins"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins metodo. Specifica i margini intorno alle pagine in un documento HTML. Il valore dei margini è misurato in punti e deve essere uguale o maggiore di 0. Il valore predefinito è 10 punti in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.saving/htmlfixedsaveoptions/get_pagemargins/
---
## HtmlFixedSaveOptions::get_PageMargins method


Specifica i margini attorno alle pagine in un documento HTML. Il valore dei margini è misurato in punti e deve essere uguale o superiore a 0. Il valore predefinito è 10 punti.

```cpp
double Aspose::Words::Saving::HtmlFixedSaveOptions::get_PageMargins() const
```

## Note


Dipende dal valore della proprietà [PageHorizontalAlignment](../get_pagehorizontalalignment/):

* Defines top, bottom and left page margins if the value is [Left](../../htmlfixedpagehorizontalalignment/).
* Defines top, bottom and right page margins if the value is [Right](../../htmlfixedpagehorizontalalignment/).
* Defines top and bottom page margins if the value is [Center](../../htmlfixedpagehorizontalalignment/).



## Esempi



Mostra come regolare i margini di pagina durante il salvataggio di un documento in HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_PageMargins(15);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.PageMargins/styles.css");

ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }")->get_Success());
```

## Vedi anche

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
