---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory méthode"
linktitle: "get_BuildingBlockCategory"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory méthode. Spécifie la catégorie de bloc de construction pour ce nœud SDT. Ne peut pas être null en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.markup/structureddocumenttag/get_buildingblockcategory/
---
## StructuredDocumentTag::get_BuildingBlockCategory method


Spécifie la catégorie du bloc de construction pour ce nœud **SDT**. Ne peut pas être **null**.

```cpp
System::String Aspose::Words::Markup::StructuredDocumentTag::get_BuildingBlockCategory()
```

## Remarques


L'accès à cette propriété ne fonctionnera que pour les types de SDT [BuildingBlockGallery](../../sdttype/) et [DocPartObj](../../sdttype/). Elle est en lecture seule pour les **SDT** de type partie de document.

Pour tous les autres types de SDT, une exception se produira.

## Exemples



Montre comment insérer une balise de document structuré en tant que bloc de construction, et définir sa catégorie et sa galerie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto buildingBlockSdt = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::BuildingBlockGallery, Aspose::Words::Markup::MarkupLevel::Block);
buildingBlockSdt->set_BuildingBlockCategory(u"Built-in");
buildingBlockSdt->set_BuildingBlockGallery(u"Table of Contents");

doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag>>(buildingBlockSdt);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.BuildingBlockCategories.docx");
```

## Voir aussi

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
