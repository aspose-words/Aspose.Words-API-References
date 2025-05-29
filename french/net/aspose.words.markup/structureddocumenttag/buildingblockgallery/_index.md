---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words pour .NET
description: Découvrez la propriété StructuredDocumentTag BuildingBlockGallery, qui définit le type de bloc de construction de votre SDT. Personnalisez vos documents en toute simplicité !
type: docs
weight: 40
url: /fr/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Spécifie le type de bloc de construction pour cela**SDT** . Ne peut pas être`nul` .

```csharp
public string BuildingBlockGallery { get; set; }
```

## Remarques

L'accès à cette propriété ne fonctionnera que pourBuildingBlockGallery et DocPartObj Types SDT. Il est en lecture seule pour**SDT** du type de partie de document.

Pour tous les autres types de SDT, une exception se produira.

## Exemples

Montre comment insérer une balise de document structurée en tant que bloc de construction et définir sa catégorie et sa galerie.

```csharp
Document doc = new Document();

StructuredDocumentTag buildingBlockSdt =
    new StructuredDocumentTag(doc, SdtType.BuildingBlockGallery, MarkupLevel.Block)
    {
        BuildingBlockCategory = "Built-in",
        BuildingBlockGallery = "Table of Contents"
    };

doc.FirstSection.Body.AppendChild(buildingBlockSdt);

doc.Save(ArtifactsDir + "StructuredDocumentTag.BuildingBlockCategories.docx");
```

### Voir également

* class [StructuredDocumentTag](../)
* espace de noms [Aspose.Words.Markup](../../../aspose.words.markup/)
* Assemblée [Aspose.Words](../../../)
