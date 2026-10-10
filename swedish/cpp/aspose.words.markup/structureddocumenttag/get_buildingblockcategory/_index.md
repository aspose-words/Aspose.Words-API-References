---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory method"
linktitle: "get_BuildingBlockCategory"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory method. Anger kategori för byggblock för denna SDT‑nod. Kan inte vara null i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockcategory/
---
## StructuredDocumentTag::get_BuildingBlockCategory method


Anger kategori för byggblock för denna **SDT**-nod. Kan inte vara **null**.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory()
```

## Anmärkningar


Att komma åt den här egenskapen fungerar endast för [BuildingBlockGallery](../../sdttype/) och [DocPartObj](../../sdttype/) SDT‑typer. Den är skrivskyddad för **SDT** av dokumentdelstypen.

För alla andra SDT-typer kommer ett undantag att uppstå.

## Exempel



Visar hur man infogar en strukturerad dokumenttagg som ett byggblock och sätter dess kategori och galleri.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::BuildingBlockGallery, Aspose::Words::Markup::MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## Se även

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
