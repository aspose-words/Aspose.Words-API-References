---
title: get_BuildingBlockCategory
second_title: Aspose.Words for C++ API Reference
description: Specifies category of building block for this SDT node. Can not be null.
type: docs
weight: 66
url: /cpp/aspose.words.markup/structureddocumenttag/get_buildingblockcategory/
---
## StructuredDocumentTag::get_BuildingBlockCategory method


Specifies category of building block for this **SDT** node. Can not be **null**.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory()
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
* Library [Aspose.Words](../../../)
