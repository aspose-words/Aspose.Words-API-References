---
title: "Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng yöntemi"
linktitle: "get_ConvertMetafilesToPng"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng yöntemi. Metafile (Wmf veya Emf) görüntülerini Png görüntü formatına dönüştürüp dönüştürmeyeceğini C++'ta alır veya ayarlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.loading/loadoptions/get_convertmetafilestopng/
---
## LoadOptions::get_ConvertMetafilesToPng method


Metafile ([Wmf](../) veya [Emf](../)) görüntülerinin [Png](../) görüntü formatına dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar.

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng() const
```


## Örnekler



Belge yüklenirken WMF/EMF'yi PNG'ye nasıl dönüştüreceğinizi gösterir.
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

## Ayrıca Bakınız

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
