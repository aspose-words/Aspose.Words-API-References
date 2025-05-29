---
title: RevisionOptions.InsertCellColor
linktitle: InsertCellColor
articleTitle: InsertCellColor
second_title: Aspose.Words für .NET
description: Passen Sie Ihre Tabelle mit der InsertCellColor-Eigenschaft in RevisionOptions an. Wählen Sie Ihre bevorzugte Farbe für eingefügte Zellen – die Standardfarbe ist Blau!
type: docs
weight: 50
url: /de/net/aspose.words.layout/revisionoptions/insertcellcolor/
---
## RevisionOptions.InsertCellColor property

Ermöglicht die Angabe der Farbe, die für eingefügte Zellen verwendet werden sollInsertion . Der Standardwert istBlue .

```csharp
public RevisionColor InsertCellColor { get; set; }
```

## Beispiele

Zeigt, wie mit der Revisionsfarbe für das Einfügen/Löschen von Zellen gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Cell revisions.docx");

doc.LayoutOptions.RevisionOptions.InsertCellColor = RevisionColor.LightBlue;
doc.LayoutOptions.RevisionOptions.DeleteCellColor = RevisionColor.DarkRed;

doc.Save(ArtifactsDir + "Revision.RevisionCellColor.pdf");
```

### Siehe auch

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* namensraum [Aspose.Words.Layout](../../../aspose.words.layout/)
* Montage [Aspose.Words](../../../)
