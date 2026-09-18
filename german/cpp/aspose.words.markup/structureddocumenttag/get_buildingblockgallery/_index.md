---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery-Methode"
linktitle: "get_BuildingBlockGallery"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery-Methode. Gibt den Typ des Bausteins für dieses SDT an. Darf in C++ nicht null sein."
type: docs
weight: 7000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockgallery/
---
## StructuredDocumentTag::get_BuildingBlockGallery method


Gibt den Typ des Bausteins für dieses **SDT** an. Darf nicht **null** sein.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockGallery()
```

## Hinweise


Der Zugriff auf diese Eigenschaft funktioniert nur für die SDT‑Typen [BuildingBlockGallery](../../sdttype/) und [DocPartObj](../../sdttype/). Sie ist schreibgeschützt für **SDT** des Dokumentteiltyps.

Für alle anderen SDT‑Typen wird eine Ausnahme auftreten.

## Beispiele



Zeigt, wie man ein strukturiertes Dokument-Tag als Baustein einfügt und dessen Kategorie und Galerie festlegt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::BuildingBlockGallery, Aspose::Words::Markup::MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## Siehe auch

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
