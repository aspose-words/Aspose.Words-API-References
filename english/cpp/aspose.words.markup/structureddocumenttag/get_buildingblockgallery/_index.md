---
title: Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery method
linktitle: get_BuildingBlockGallery
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery method. Specifies type of building block for this SDT. Can not be null in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.markup/structureddocumenttag/get_buildingblockgallery/
---
## StructuredDocumentTag::get_BuildingBlockGallery method


Specifies type of building block for this **SDT**. Can not be **null**.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery()
```

## Remarks


Accessing this property will only work for [BuildingBlockGallery](../../sdttype/) and [DocPartObj](../../sdttype/) SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

## Examples



Shows how to insert a structured document tag as a building block, and set its category and gallery. 
```cpp
auto doc = MakeObject<Document>();

auto buildingBlockSdt = MakeObject<StructuredDocumentTag>(doc, SdtType::BuildingBlockGallery, MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild(buildingBlockSdt);

doc->Save(ArtifactsDir + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
