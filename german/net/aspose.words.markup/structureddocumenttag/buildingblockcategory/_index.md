---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „StructuredDocumentTag BuildingBlockCategory“, die für die Definition von Bausteinkategorien in SDT-Knoten unerlässlich ist. Verbessern Sie Ihre Dokumentstruktur!
type: docs
weight: 30
url: /de/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Gibt die Kategorie des Bausteins für dieses**SDT** node. Kann nicht`null` .

```csharp
public string BuildingBlockCategory { get; set; }
```

## Bemerkungen

Der Zugriff auf diese Eigenschaft funktioniert nur fürBuildingBlockGallery und DocPartObj SDT-Typen. Es ist schreibgeschützt für**SDT** des Dokumentteiltyps.

Bei allen anderen SDT-Typen tritt eine Ausnahme auf.

## Beispiele

Zeigt, wie Sie ein strukturiertes Dokument-Tag als Baustein einfügen und seine Kategorie und Galerie festlegen.

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

### Siehe auch

* class [StructuredDocumentTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
