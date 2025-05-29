---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words für .NET
description: Entdecken Sie die StructuredDocumentTag BuildingBlockGallery-Eigenschaft, die den Bausteintyp Ihres SDT definiert. Sorgen Sie für eine nahtlose Dokumentanpassung!
type: docs
weight: 40
url: /de/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Gibt den Typ des Bausteins für dieses**SDT** . Kann nicht sein`null` .

```csharp
public string BuildingBlockGallery { get; set; }
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
