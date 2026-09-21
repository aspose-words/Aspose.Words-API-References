---
title: "Aspose::Words::Font::get_Shadow metod"
linktitle: "get_Shadow"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Shadow metod. Sant om teckensnittet är formaterat som skuggat i C++."
type: docs
weight: 35000
url: /sv/cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


Sant om teckensnittet är formaterat som skuggat.

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## Exempel



Visar hur man skapar ett textstycke formaterat med en skugga.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ställ in Shadow-flaggan för att tillämpa en förskjuten skuggeffekt,
// vilket får bokstäverna att se ut som om de svävar över sidan.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
