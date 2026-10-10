---
title: "Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng metodo"
linktitle: "get_ConvertMetafilesToPng"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng metodo. Ottiene o imposta se convertire le immagini metafile(Wmf o Emf) nel formato immagine Png in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.loading/loadoptions/get_convertmetafilestopng/
---
## LoadOptions::get_ConvertMetafilesToPng method


Ottiene o imposta se convertire le immagini metafile ([Wmf](../) o [Emf](../)) nel formato immagine [Png](../).

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng() const
```


## Esempi



Mostra come convertire WMF/EMF in PNG durante il caricamento del documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateImageDirectly.docx");

shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

Aspose::Words::ApiExamples::TestUtil::VerifyImageInShape(1600, 1600, Aspose::Words::Drawing::ImageType::Wmf, shape);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_ConvertMetafilesToPng(true);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Image.CreateImageDirectly.docx", loadOptions);
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

Aspose::Words::ApiExamples::TestUtil::VerifyImageInShape(1666, 1666, Aspose::Words::Drawing::ImageType::Png, shape);
```

## Vedi anche

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
