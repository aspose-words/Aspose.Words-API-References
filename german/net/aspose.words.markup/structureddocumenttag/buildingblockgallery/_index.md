---
title: StructuredDocumentTag.BuildingBlockGallery
linktitle: BuildingBlockGallery
articleTitle: BuildingBlockGallery
second_title: Aspose.Words für .NET
description: StructuredDocumentTag BuildingBlockGallery eigendom. Gibt den Typ des Bausteins dafür anSDT . Kann nicht seinNull  in C#.
type: docs
weight: 40
url: /de/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Gibt den Typ des Bausteins dafür an**SDT** . Kann nicht sein`Null` .

```csharp
public string BuildingBlockGallery { get; set; }
```

## Bemerkungen

Der Zugriff auf diese Eigenschaft funktioniert nur fürBuildingBlockGallery and DocPartObj SDT-Typen. Es ist schreibgeschützt für**SDT** des Dokumentteiltyps.

Bei allen anderen SDT-Typen tritt eine Ausnahme auf.

## Beispiele

Zeigt, wie man ein strukturiertes Dokument-Tag als Baustein einfügt und seine Kategorie und Galerie festlegt.

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
