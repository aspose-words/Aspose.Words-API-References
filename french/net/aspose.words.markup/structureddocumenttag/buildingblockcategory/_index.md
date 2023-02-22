---
title: StructuredDocumentTag.BuildingBlockCategory
second_title: Référence de l'API Aspose.Words pour .NET
description: StructuredDocumentTag propriété. Spécifie la catégorie de bloc de construction pour ce TDS node. Ne peut pas être null.
type: docs
weight: 30
url: /fr/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Spécifie la catégorie de bloc de construction pour ce **TDS** node. Ne peut pas être null.

```csharp
public string BuildingBlockCategory { get; set; }
```

### Remarques

L'accès à cette propriété ne fonctionnera que pourBuildingBlockGallery et DocPartObj Type SDT. Il est en lecture seule pour **TDS**du type de partie de document.

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


