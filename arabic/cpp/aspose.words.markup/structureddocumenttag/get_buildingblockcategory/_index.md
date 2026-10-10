---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory طريقة"
linktitle: "get_BuildingBlockCategory"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory. تحدد فئة كتلة البناء لهذا العقدة من نوع SDT. لا يمكن أن تكون null في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockcategory/
---
## StructuredDocumentTag::get_BuildingBlockCategory method


يحدد فئة كتلة البناء لهذه العقدة **SDT**. لا يمكن أن تكون **null**.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory()
```

## ملاحظات


الوصول إلى هذه الخاصية سيعمل فقط مع أنواع SDT الخاصة بـ [BuildingBlockGallery](../../sdttype/) و [DocPartObj](../../sdttype/). وهي للقراءة فقط للـ **SDT** من نوع جزء المستند.

ستحدث استثناء لجميع أنواع SDT الأخرى.

## أمثلة



يوضح كيفية إدراج علامة مستند منسقة ككتلة بناء، وتعيين فئتها ومعرضها.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::BuildingBlockGallery, Aspose::Words::Markup::MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## انظر أيضًا

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
