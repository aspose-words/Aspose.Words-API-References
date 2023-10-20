---
title: StructuredDocumentTag.BuildingBlockCategory
linktitle: BuildingBlockCategory
articleTitle: BuildingBlockCategory
second_title: Aspose.Words für .NET
description: StructuredDocumentTag BuildingBlockCategory eigendom. Gibt die Kategorie des Bausteins dafür anSDT node. Kann nicht seinNull  in C#.
type: docs
weight: 30
url: /de/net/aspose.words.markup/structureddocumenttag/buildingblockcategory/
---
## StructuredDocumentTag.BuildingBlockCategory property

Gibt die Kategorie des Bausteins dafür an**SDT** node. Kann nicht sein`Null` .

```csharp
public string BuildingBlockCategory { get; set; }
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
