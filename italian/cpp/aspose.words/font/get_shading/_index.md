---
title: "Aspose::Words::Font::get_Shading metodo"
linktitle: "get_Shading"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Font::get_Shading metodo. Restituisce un oggetto Shading che si riferisce alla formattazione dell'ombreggiatura per il carattere in C++."
type: docs
weight: 34000
url: /it/cpp/aspose.words/font/get_shading/
---
## Font::get_Shading method


Restituisce un oggetto [Shading](../../shading/) che si riferisce alla formattazione dell'ombreggiatura per il carattere.

```cpp
System::SharedPtr<Aspose::Words::Shading> Aspose::Words::Font::get_Shading()
```


## Esempi



Mostra come applicare l'ombreggiatura al testo creato da un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Color(System::Drawing::Color::get_White());

// Un modo per rendere visibile il testo creato usando il nostro colore del carattere bianco
// è applicare un effetto di ombreggiatura di sfondo.
System::SharedPtr<Aspose::Words::Shading> shading = builder->get_Font()->get_Shading();
shading->set_Texture(Aspose::Words::TextureIndex::TextureDiagonalUp);
shading->set_BackgroundPatternColor(System::Drawing::Color::get_OrangeRed());
shading->set_ForegroundPatternColor(System::Drawing::Color::get_DarkBlue());

builder->Writeln(u"White text on an orange background with a two-tone texture.");

doc->Save(get_ArtifactsDir() + u"Font.Shading.docx");
```

## Vedi anche

* Class [Shading](../../shading/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
