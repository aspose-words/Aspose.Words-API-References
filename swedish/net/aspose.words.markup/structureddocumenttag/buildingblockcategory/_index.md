---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: Aspose.Words för .NET
description: Upptäck egenskapen BuildingBlockCategory i StructuredDocumentTag, som är viktig för att definiera byggstenskategorier i SDT-noder. Förbättra din dokumentstruktur!
type: docs
weight: 30
url: /sv/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Anger kategori för byggsten för detta**SDT** nod. Kan inte vara`null` .

```csharp
public string BuildingBlockCategory { get; set; }
```

## Anmärkningar

Åtkomst till den här egendomen fungerar endast förBuildingBlockGallery och DocPartObj SDT-typer. Den är skrivskyddad för**SDT** av dokumentdelstypen.

För alla andra SDT-typer kommer undantag att inträffa.

## Exempel

Visar hur man infogar en strukturerad dokumenttagg som en byggsten och anger dess kategori och galleri.

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
