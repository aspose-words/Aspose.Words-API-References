---
title: "Aspose::Words::ParagraphFormat::get_WordWrap‑Methode"
linktitle: "get_WordWrap"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_WordWrap‑Methode. Wenn diese Eigenschaft false ist, kann lateinischer Text in der Mitte eines Wortes für den aktuellen Absatz umgebrochen werden. Andernfalls wird lateinischer Text in C++ wortweise umgebrochen."
type: docs
weight: 42000
url: /de/cpp/aspose.words/paragraphformat/get_wordwrap/
---
## ParagraphFormat::get_WordWrap method


Wenn diese Eigenschaft **false** ist, kann lateinischer Text in der Mitte eines Wortes im aktuellen Absatz umgebrochen werden. Andernfalls wird lateinischer Text wortweise umbrochen.

```cpp
bool Aspose::Words::ParagraphFormat::get_WordWrap()
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
