---
title: "Aspose::Words::ParagraphFormat::get_WordWrap‑metod"
linktitle: "get_WordWrap"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ParagraphFormat::get_WordWrap‑metod. Om den här egenskapen är falsk kan latinsk text i mitten av ett ord radbrytas för det aktuella stycket. Annars radbryts latinsk text efter hela ord i C++."
type: docs
weight: 42000
url: /sv/cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


Om den här egenskapen är **false** kan latinsk text i mitten av ett ord radbrytas i det aktuella stycket. Annars radbryts latinsk text efter hela ord.

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
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
