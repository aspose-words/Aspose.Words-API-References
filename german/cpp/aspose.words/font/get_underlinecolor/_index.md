---
title: "Aspose::Words::Font::get_UnderlineColor Methode"
linktitle: "get_UnderlineColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Font::get_UnderlineColor Methode. Gibt die Farbe der Unterstreichung zurück oder legt sie fest, die auf die Schriftart in C++ angewendet wird."
type: docs
weight: 56000
url: /de/cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


Ruft ab oder legt fest die Farbe der Unterstreichung, die auf die Schriftart angewendet wird.

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## Beispiele



Zeigt, wie man den Stil und die Farbe einer Textunterstreichung konfiguriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## Siehe auch

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
