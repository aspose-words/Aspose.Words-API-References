---
title: "Aspose::Words::Font::get_Outline Methode"
linktitle: "get_Outline"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_Outline Methode. True, wenn die Schriftart als Kontur formatiert ist in C++."
type: docs
weight: 31000
url: /de/cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


Wahr, wenn die Schriftart als Kontur formatiert ist.

```cpp
bool Aspose::Words::Font::get_Outline()
```


## Beispiele



Zeigt, wie man einen Textlauf erstellt, der als Kontur formatiert ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Setzen Sie das Outline-Flag, um die Füllfarbe des Textes auf Weiß zu ändern und
// lassen Sie eine dünne Kontur um jedes Zeichen in der ursprünglichen Farbe des Textes.
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(get_ArtifactsDir() + u"Font.Outline.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
