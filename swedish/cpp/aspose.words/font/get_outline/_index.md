---
title: "Aspose::Words::Font::get_Outline metod"
linktitle: "get_Outline"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Outline metod. Sant om teckensnittet är formaterat som kontur i C++."
type: docs
weight: 31000
url: /sv/cpp/aspose.words/font/get_outline/
---
## Font::get_Outline method


Sant om teckensnittet är formaterat som kontur.

```cpp
bool Aspose::Words::Font::get_Outline()
```


## Exempel



Visar hur man skapar ett textstycke formaterat som kontur.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ställ in Outline-flagg för att ändra textens fyllningsfärg till vit och
// lämna en tunn kontur runt varje tecken i textens ursprungliga färg.
builder->get_Font()->set_Outline(true);
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has an outline.");

doc->Save(get_ArtifactsDir() + u"Font.Outline.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
