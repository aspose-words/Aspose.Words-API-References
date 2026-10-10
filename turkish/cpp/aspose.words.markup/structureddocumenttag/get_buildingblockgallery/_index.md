---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery metodu"
linktitle: "get_BuildingBlockGallery"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery metodu. Bu **SDT** için yapı bloğu türünü belirtir. C++'ta null olamaz."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockgallery/
---
## StructuredDocumentTag::get_BuildingBlockGallery method


Bu **SDT** için yapı bloğu tipini belirtir. **null** olamaz.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery()
```

## Açıklamalar


Bu özelliğe erişim yalnızca [BuildingBlockGallery](../../sdttype/) ve [DocPartObj](../../sdttype/) SDT türleri için çalışır. Belge parçası türündeki **SDT** için yalnızca okunabilir.

Diğer tüm SDT türleri için bir istisna oluşacaktır.

## Örnekler



Bir yapılandırılmış belge etiketini yapı bloğu olarak eklemeyi ve onun kategorisini ve galerisini ayarlamayı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::BuildingBlockGallery, Aspose::Words::Markup::MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## Ayrıca Bakınız

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
