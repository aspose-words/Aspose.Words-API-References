---
title: "Aspose::Words::Saving::ImageSaveOptions::get_Scale metodo"
linktitle: "get_Scale"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_Scale metodo. Ottiene o imposta il fattore di zoom per le immagini generate in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.saving/imagesaveoptions/get_scale/
---
## ImageSaveOptions::get_Scale method


Ottiene o imposta il fattore di zoom per le immagini generate.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_Scale() const
```


## Esempi



Mostra come modificare l'immagine mentre Aspose.Words converte un documento in una.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// modifica l'immagine mentre l'operazione di salvataggio la rende.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Possiamo regolare queste proprietà per modificare la luminosità e il contrasto dell'immagine.
// Entrambe sono su una scala da 0 a 1 e sono impostate a 0.5 per impostazione predefinita.
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
// Possiamo regolare la risoluzione orizzontale e verticale con queste proprietà.
// Ciò influenzerà le dimensioni dell'immagine.
// Il valore predefinito per queste proprietà è 96.0, per una risoluzione di 96dpi.
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
// Possiamo ridimensionare l'immagine usando questa proprietà. Il valore predefinito è 1.0, per una scala del 100%.
// Possiamo usare questa proprietà per annullare eventuali modifiche alle dimensioni dell'immagine che il cambiamento della risoluzione potrebbe causare.
options->set_Scale(96.f / 72.f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.EditImage.png", options);
```


Mostra come renderizzare un oggetto Office [Math](../../../aspose.words.math/) in un file immagine nel file system locale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto math = System::ExplicitCast<Aspose::Words::Math::OfficeMath>(doc->GetChild(Aspose::Words::NodeType::OfficeMath, 0, true));

// Crea un oggetto "ImageSaveOptions" da passare al metodo "Save" del renderer del nodo per modificare
// come renderizza il nodo OfficeMath in un'immagine.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);

// Imposta la proprietà "Scale" a 5 per renderizzare l'oggetto a cinque volte la sua dimensione originale.
saveOptions->set_Scale(5.0f);

math->GetMathRenderer()->Save(get_ArtifactsDir() + u"Shape.RenderOfficeMath.png", saveOptions);
```

## Vedi anche

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
