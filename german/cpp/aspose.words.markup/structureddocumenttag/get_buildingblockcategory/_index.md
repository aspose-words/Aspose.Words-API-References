---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory Methode"
linktitle: "get_BuildingBlockCategory"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory Methode. Gibt die Kategorie des Bausteins für diesen SDT‑Knoten an. Darf in C++ nicht null sein."
type: docs
weight: 6000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockcategory/
---
## StructuredDocumentTag::get_BuildingBlockCategory method


Gibt die Kategorie des Bausteins für diesen **SDT**‑Knoten an. Darf nicht **null** sein.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory()
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
