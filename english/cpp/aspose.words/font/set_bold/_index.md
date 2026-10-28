---
title: Aspose::Words::Font::set_Bold method
linktitle: set_Bold
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::set_Bold method. True if the font is formatted as bold in C++.'
type: docs
weight: 62000
url: /cpp/aspose.words/font/set_bold/
---
## Font::set_Bold method


True if the font is formatted as bold.

```cpp
void Aspose::Words::Font::set_Bold(bool value)
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
## See Also

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
