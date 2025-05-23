---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: Aspose.Words for .NET
description: Discover the StructuredDocumentTag BuildingBlockCategory property, essential for defining building block categories in SDT nodes. Enhance your document structure!
type: docs
weight: 30
url: /net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Specifies category of building block for this **SDT** node. Can not be `null`.

```csharp
public string BuildingBlockCategory { get; set; }
```

## Remarks

Accessing this property will only work for BuildingBlockGallery and DocPartObj SDT types. It is read-only for **SDT** of the document part type.

For all other SDT types exception will occur.

## Examples

Shows how to insert a structured document tag as a building block, and set its category and gallery.

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

### See Also

* class [StructuredDocumentTag](../)
* namespace [Aspose.Words.Markup](../../../aspose.words.markup/)
* assembly [Aspose.Words](../../../)
