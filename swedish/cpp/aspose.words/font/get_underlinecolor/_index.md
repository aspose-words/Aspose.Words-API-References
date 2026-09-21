---
title: "Aspose::Words::Font::get_UnderlineColor metod"
linktitle: "get_UnderlineColor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_UnderlineColor metod. Hämtar eller anger färgen på understrykningen som appliceras på teckensnittet i C++."
type: docs
weight: 56000
url: /sv/cpp/aspose.words/font/get_underlinecolor/
---
## Font::get_UnderlineColor method


Hämtar eller anger färgen på understrykningen som tillämpas på teckensnittet.

```cpp
System::Drawing::Color Aspose::Words::Font::get_UnderlineColor()
```


## Exempel



Visar hur man konfigurerar stil och färg på en textunderstrykning.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
