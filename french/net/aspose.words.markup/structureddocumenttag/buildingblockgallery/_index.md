---
title: StructuredDocumentTag.BuildingBlockGallery
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTag propriété. Spécifie le type de bloc de construction pour cela TSD . Ne peut pas êtrenul .
type: docs
weight: 40
url: /fr/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Spécifie le type de bloc de construction pour cela **TSD** . Ne peut pas être`nul` .

```csharp
public string BuildingBlockGallery { get; set; }
```

### Remarques

L'accès à cette propriété ne fonctionnera que pourBuildingBlockGallery et DocPartObj Types SDT. Il est en lecture seule pour **TSD** du type de partie de document.

Pour tous les autres types de SDT, une exception se produira.

### Exemples

Montre comment insérer une balise de document structuré en tant que bloc de construction et définir sa catégorie et sa galerie.

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
* espace de noms [Aspose.Words.Markup](../../structureddocumenttag/)
* Assemblée [Aspose.Words](../../../)


