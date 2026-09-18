---
title: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl Methode"
linktitle: "get_FarEastLineBreakControl"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl-Methode. Gibt ein Flag zurück oder legt es fest, das angibt, ob ostasiatische Zeilenumbruchregeln auf den aktuellen Absatz in C++ angewendet werden."
type: docs
weight: 12000
url: /de/cpp/aspose.words/paragraphformat/get_fareastlinebreakcontrol/
---
## ParagraphFormat::get_FarEastLineBreakControl method


Liest oder legt ein Flag fest, das angibt, ob ostasiatische Zeilenumbruchregeln auf den aktuellen Absatz angewendet werden.

```cpp
bool Aspose::Words::ParagraphFormat::get_FarEastLineBreakControl()
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
