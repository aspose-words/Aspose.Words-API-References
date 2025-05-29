---
title: RevisionOptions.DeleteCellColor
linktitle: DeleteCellColor
articleTitle: DeleteCellColor
second_title: Aspose.Words för .NET
description: Anpassa ditt kalkylblad med egenskapen DeleteCellColor i RevisionOptions. Ställ enkelt in en unik färg för borttagna celler, vilket förbättrar tydlighet och organisation.
type: docs
weight: 20
url: /sv/net/aspose.words.layout/revisionoptions/deletecellcolor/
---
## RevisionOptions.DeleteCellColor property

Gör det möjligt att ange färgen som ska användas för borttagna cellerDeletion . Standardvärdet ärPink .

```csharp
public RevisionColor DeleteCellColor { get; set; }
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
