---
title: Aspose::Words::Font::set_UnderlineColor method
linktitle: set_UnderlineColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_UnderlineColor method. Sets the color of the underline applied to the font in C++.'
type: docs
weight: 108000
url: /cpp/aspose.words/font/set_underlinecolor/
---
## Font::set_UnderlineColor method


Sets the color of the underline applied to the font.

```cpp
void Aspose::Words::Font::set_UnderlineColor(System::Drawing::Color value)
```

## Examples


Shows how to configure the style and color of a text underline.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
