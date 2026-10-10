---
title: "Aspose::Words::ParagraphFormat::get_MirrorIndents Methode"
linktitle: "get_MirrorIndents"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::ParagraphFormat::get_MirrorIndents Methode. Ruft einen Wert ab oder legt ihn fest, der angibt, ob die linken und rechten Einzüge dieselbe Breite in C++ haben."
type: docs
weight: 24500
url: /de/cpp/aspose.words/paragraphformat/get_mirrorindents/
---
## ParagraphFormat::get_MirrorIndents method


Liest oder legt ein Flag fest, das angibt, ob der linke und rechte Einzug die gleiche Breite haben.

```cpp
bool Aspose::Words::ParagraphFormat::get_MirrorIndents()
```


## Beispiele



Zeigen Sie, wie man linke und rechte Einzüge gleich macht.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");
System::SharedPtr<Aspose::Words::ParagraphFormat> format = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_ParagraphFormat();

format->set_MirrorIndents(true);

doc->Save(get_ArtifactsDir() + u"ParagraphFormat.MirrorIndents.docx");
```

## Siehe auch

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
