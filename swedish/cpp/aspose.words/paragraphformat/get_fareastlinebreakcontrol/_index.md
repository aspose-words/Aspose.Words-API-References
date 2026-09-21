---
title: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl metod"
linktitle: "get_FarEastLineBreakControl"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl metod. Hämtar eller anger en flagga som indikerar om östasiatiska radbrytningsregler tillämpas på det aktuella stycket i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/paragraphformat/get_fareastlinebreakcontrol/
---
## ParagraphFormat::get_FarEastLineBreakControl method


Hämtar eller anger en flagga som indikerar om östasiatiska radbrytningsregler tillämpas på det aktuella stycket.

```cpp
bool Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl()
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
