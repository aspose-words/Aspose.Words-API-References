---
title: Aspose::Words::Font::set_Size method
linktitle: set_Size
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_Size method. Sets the font size in points in C++.'
type: docs
weight: 88000
url: /cpp/aspose.words/font/set_size/
---
## Font::set_Size method


Sets the font size in points.

```cpp
void Aspose::Words::Font::set_Size(double value)
```

## Examples


Shows how to insert formatted text using DocumentBuilder.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Specify font formatting, then add text.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Underline::Dash);

builder->Write(u"Hello world!");
```

Shows how to format a run of text using its font property.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
