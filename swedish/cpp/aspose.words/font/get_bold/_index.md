---
title: "Aspose::Words::Font::get_Bold metod"
linktitle: "get_Bold"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Bold metod. Sant om teckensnittet är formaterat som fetstil i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words/font/get_bold/
---
## Font::get_Bold method


Sant om teckensnittet är formaterat som fetstil.

```cpp
bool Aspose::Words::Font::get_Bold()
```


## Exempel



Visar hur man infogar formaterad text med hjälp av [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ange teckensnittformatering, och lägg sedan till text.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
