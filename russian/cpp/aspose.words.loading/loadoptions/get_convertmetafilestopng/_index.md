---
title: "Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng метод"
linktitle: "get_ConvertMetafilesToPng"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng метод. Получает или задает, следует ли преобразовывать изображения метафайлов (Wmf или Emf) в формат изображения Png в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.loading/loadoptions/get_convertmetafilestopng/
---
## LoadOptions::get_ConvertMetafilesToPng method


Получает или задает, следует ли конвертировать метафайлы ([Wmf](../) или [Emf](../)) в формат изображения [Png](../).

```cpp
bool Aspose::Words::Loading::LoadOptions::get_ConvertMetafilesToPng() const
```


## Примеры



Показывает, как преобразовать WMF/EMF в PNG при загрузке документа.
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

## См. также

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
