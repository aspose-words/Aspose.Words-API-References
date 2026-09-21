---
title: "Aspose::Words::ParagraphFormat::get_HangingPunctuation metod"
linktitle: "get_HangingPunctuation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_HangingPunctuation metod. Hämtar eller anger en flagga som indikerar huruvida hängande interpunktion är aktiverad för den aktuella paragrafen i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words/paragraphformat/get_hangingpunctuation/
---
## ParagraphFormat::get_HangingPunctuation method


Hämtar eller anger en flagga som indikerar om hängande interpunktion är aktiverad för det aktuella stycket.

```cpp
bool Aspose::Words::ParagraphFormat::get_HangingPunctuation()
```


## Exempel



Visar hur man ställer in speciella egenskaper för asiatisk typografi.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## Se även

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
