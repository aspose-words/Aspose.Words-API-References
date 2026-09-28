---
title: "Метод Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery"
linktitle: "get_BuildingBlockGallery"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery. Указывает тип строительного блока для этого **SDT**. Не может быть null в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockgallery/
---
## StructuredDocumentTag::get_BuildingBlockGallery method


Указывает тип строительного блока для этого **SDT**. Не может быть **null**.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery()
```

## Примечания


Доступ к этому свойству будет работать только для типов SDT [BuildingBlockGallery](../../sdttype/) и [DocPartObj](../../sdttype/). Оно доступно только для чтения для **SDT** типа части документа.

Для всех остальных типов SDT будет возникать исключение.

## Примеры



Показано, как вставить структурный тег документа в качестве строительного блока и задать его категорию и галерею.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::BuildingBlockGallery, Aspose::Words::Markup::MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## См. также

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
