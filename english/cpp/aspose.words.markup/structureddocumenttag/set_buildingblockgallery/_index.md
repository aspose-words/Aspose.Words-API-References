---
title: Aspose::Words::Markup::StructuredDocumentTag::set_BuildingBlockGallery method
linktitle: set_BuildingBlockGallery
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Markup::StructuredDocumentTag::set_BuildingBlockGallery method. Specifies type of building block for this SDT. Can not be null in C++.'
type: docs
weight: 95000
url: /cpp/aspose.words.markup/structureddocumenttag/set_buildingblockgallery/
---
## StructuredDocumentTag::set_BuildingBlockGallery method


Specifies type of building block for this SDT. Can not be **null**.

```cpp
void Aspose::Words::Markup::StructuredDocumentTag::set_BuildingBlockGallery(const System::String & value)
```

## Remarks


Accessing this property will only work for [BuildingBlockGallery](../../sdttype/) and [DocPartObj](../../sdttype/) SDT types. It is read-only for SDT of the document part type. 

For all other SDT types exception will occur.
## Examples


Shows how to insert a structured document tag as a building block, and set its category and gallery.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, SdtType::BuildingBlockGallery, MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```
## See Also

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
