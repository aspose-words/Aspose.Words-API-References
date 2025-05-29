---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: Aspose.Words för .NET
description: Anpassa ditt kalkylblad med egenskapen InsertCellColor i RevisionOptions. Välj önskad färg för infogade celler – standard är blå!
type: docs
weight: 50
url: /sv/net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

Gör det möjligt att ange färgen som ska användas för infogade cellerInsertion . Standardvärdet ärBlue .

```csharp
public RevisionColor InsertCellColor { get; set; }
```

## Exempel

Visar hur man arbetar med revisionsfärgen för att infoga/ta bort celler.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### Se även

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* namnutrymme [Aspose.Words.Layout](../../../aspose.words.layout/)
* hopsättning [Aspose.Words](../../../)
