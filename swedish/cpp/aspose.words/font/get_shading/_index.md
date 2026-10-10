---
title: "Aspose::Words::Font::get_Shading metod"
linktitle: "get_Shading"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Font::get_Shading metod. Returnerar ett Shading‑objekt som hänvisar till skuggningsformateringen för teckensnittet i C++."
type: docs
weight: 34000
url: /sv/cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


Returnerar ett [Shading](../../shading/)‑objekt som hänvisar till skuggningsformateringen för teckensnittet.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## Exempel



Visar hur man applicerar skuggning på text som skapats av en dokumentbyggare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// Ett sätt att göra texten som skapats med vår vita teckensnittsfärg synlig
// är att applicera en bakgrundsskuggningseffekt.
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## Se även

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
