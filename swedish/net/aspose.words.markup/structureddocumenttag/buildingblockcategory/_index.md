---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: Aspose.Words för .NET
description: StructuredDocumentTag BuildingBlockCategory fast egendom. Anger kategori av byggblock för dettaSDT node. Kan inte varanull  i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Anger kategori av byggblock för detta**SDT** node. Kan inte vara`null` .

```csharp
public string BuildingBlockCategory { get; set; }
```

## Anmärkningar

Åtkomst till den här egenskapen fungerar bara förBuildingBlockGallery och DocPartObj SDT-typer. Den är skrivskyddad för**SDT** av typen dokumentdel.

För alla andra SDT-typer kommer undantag att förekomma.

## Exempel

Visar hur man infogar en strukturerad dokumenttagg som ett byggblock och ställer in dess kategori och galleri.

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

### Se även

* class [StructuredDocumentTag](../)
* namnutrymme [Aspose.Words.Markup](../../../aspose.words.markup/)
* hopsättning [Aspose.Words](../../../)
