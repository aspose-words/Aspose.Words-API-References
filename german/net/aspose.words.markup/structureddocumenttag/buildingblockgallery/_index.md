---
title: StructuredDocumentTag.BuildingBlockGallery
second_title: Aspose.Words für .NET-API-Referenz
description: StructuredDocumentTag eigendom. Gibt den Typ des Bausteins dafür an SDT . darf nicht null sein.
type: docs
weight: 40
url: /de/net/aspose.words.markup/structureddocumenttag/buildingblockgallery/
---
## StructuredDocumentTag.BuildingBlockGallery property

Gibt den Typ des Bausteins dafür an **SDT** . darf nicht null sein.

```csharp
public string BuildingBlockGallery { get; set; }
```

### Bemerkungen

Der Zugriff auf diese Eigenschaft funktioniert nur fürBuildingBlockGallery and DocPartObj SDT-Typen. Es ist schreibgeschützt für **SDT**vom Dokumentteiltyp.

Für alle anderen SDT-Typen tritt eine Ausnahme auf.

### Beispiele

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
* namensraum [Aspose.Words.Markup](../../structureddocumenttag/)
* Montage [Aspose.Words](../../../)


