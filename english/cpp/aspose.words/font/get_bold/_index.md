---
title: Aspose::Words::Font::get_Bold method
linktitle: get_Bold
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_Bold method. True if the font is formatted as bold in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


True if the font is formatted as bold.

```cpp
bool Aspose::Words::Font::get_Bold()
```


## Examples



Shows how to insert formatted text using [DocumentBuilder](../../documentbuilder/). 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Specify font formatting, then add text.
SharedPtr<Aspose::Words::Font> font = builder->get_Font();
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
