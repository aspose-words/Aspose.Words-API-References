---
title: "Aspose::Words::ParagraphFormat::get_HangingPunctuation Methode"
linktitle: "get_HangingPunctuation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_HangingPunctuation Methode. Ruft einen Wert ab oder legt ihn fest, der angibt, ob hängende Interpunktion für den aktuellen Absatz in C++ aktiviert ist."
type: docs
weight: 14000
url: /de/cpp/aspose.words/paragraphformat/get_hangingpunctuation/
---
## ParagraphFormat::get_HangingPunctuation method


Liest oder legt ein Flag fest, das angibt, ob hängende Interpunktion für den aktuellen Absatz aktiviert ist.

```cpp
bool Aspose::Words::ParagraphFormat::get_HangingPunctuation()
```


## Beispiele



Zeigt, wie man spezielle Eigenschaften für asiatische Typografie festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat();
format->set_FarEastLineBreakControl(true);
format->set_WordWrap(false);
format->set_HangingPunctuation(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.AsianTypographyProperties.docx");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
