---
title: "Aspose::Words::DocumentBuilder::get_Underline Methode"
linktitle: "get_Underline"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::get_Underline Methode. Liest/legt den Unterstreichungstyp für die aktuelle Schrift in C++ fest."
type: docs
weight: 26000
url: /de/cpp/aspose.words/documentbuilder/get_underline/
---
## DocumentBuilder::get_Underline method


Liest/setzt den Unterstreichungstyp für die aktuelle Schrift.

```cpp
Aspose::Words::Underline Aspose::Words::DocumentBuilder::get_Underline()
```


## Beispiele



Zeigt, wie Text, der von einem DocumentBuilder eingefügt wurde, formatiert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Dash);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(32);

// Der Builder wendet die Formatierung auf seinen aktuellen Absatz und jeden danach hinzugefügten Text an.
builder->Writeln(u"Large, blue, and underlined text.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertUnderline.docx");
```

## Siehe auch

* Enum [Underline](../../underline/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
