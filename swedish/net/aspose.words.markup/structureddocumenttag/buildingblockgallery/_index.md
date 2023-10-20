---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words för .NET
description: StructuredDocumentTag BuildingBlockGallery fast egendom. Anger typ av byggblock för dettaSDT . Kan inte varanull  i C#.
type: docs
weight: 40
url: /sv/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Anger typ av byggblock för detta**SDT** . Kan inte vara`null` .

```csharp
public string BuildingBlockGallery { get; set; }
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
