---
title: "Aspose::Words::Font::get_Emboss method"
linktitle: "get_Emboss"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Emboss method. Sant om teckensnittet är formaterat som upphöjt i C++."
type: docs
weight: 12000
url: /sv/cpp/aspose.words/font/get_emboss/
---
## Font::get_Emboss method


Sant om teckensnittet är formaterat som präglat.

```cpp
bool Aspose::Words::Font::get_Emboss()
```


## Exempel



Visar hur man applicerar gravyr-/präglingseffekter på text.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Color(System::Drawing::Color::get_LightBlue());

// Nedan finns två sätt att använda skuggor för att applicera en 3D-liknande effekt på texten.
// 1 -  Gravera text så att det ser ut som om bokstäverna är nedsänkta i sidan:
builder->get_Font()->set_Engrave(true);

builder->Writeln(u"This text is engraved.");

// 2 -  Prägla text så att det ser ut som om bokstäverna sticker ut från sidan:
builder->get_Font()->set_Engrave(false);
builder->get_Font()->set_Emboss(true);

builder->Writeln(u"This text is embossed.");

doc->Save(get_ArtifactsDir() + u"Font.EngraveEmboss.docx");
```

## Se även

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
