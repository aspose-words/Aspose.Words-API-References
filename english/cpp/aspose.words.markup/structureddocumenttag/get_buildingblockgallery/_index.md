---
title: get_BuildingBlockGallery
second_title: Aspose.Words for C++ API Reference
description: Specifies type of building block for this SDT. Can not be null.
type: docs
weight: 66
url: /cpp/aspose.words.markup/structureddocumenttag/get_buildingblockgallery/
---
## StructuredDocumentTag.get_BuildingBlockGallery method


Specifies type of building block for this **SDT**. Can not be null.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery()
```


Accessing this property will only work for **BuildingBlockGallery** and **DocPartObj** SDT types. It is read-only for **SDT** of the document part type.

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

