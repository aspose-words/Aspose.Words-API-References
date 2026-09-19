---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery"
linktitle: "get_BuildingBlockGallery"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery. Specifica il tipo di blocco di costruzione per questo **SDT**. Non può essere null in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockgallery/
---
## StructuredDocumentTag::get_BuildingBlockGallery method


Specifica il tipo di blocco di costruzione per questo **SDT**. Non può essere **null**.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery()
```

## Note


L'accesso a questa proprietà funziona solo per i tipi SDT [BuildingBlockGallery](../../sdttype/) e [DocPartObj](../../sdttype/). È di sola lettura per **SDT** del tipo parte del documento.

Per tutti gli altri tipi SDT si verificherà un'eccezione.

## Esempi



Mostra come inserire un tag di documento strutturato come blocco di costruzione e impostare la sua categoria e galleria.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::BuildingBlockGallery, Aspose::Words::Markup::MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## Vedi anche

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
