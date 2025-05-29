---
title: TabStop.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „TabStop-Position“, um Tabstopppositionen einfach in Punkten zu finden und so die Präzision Ihres Layouts und die Effizienz Ihres Designs zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words/tabstop/position/
---
## TabStop.Position property

Ruft die Position des Tabulatorstopps in Punkten ab.

```csharp
public double Position { get; }
```

## Beispiele

Zeigt, wie die Position des rechten Tabstopps in Inhaltsverzeichnis-bezogenen Absätzen geändert wird.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Durchlaufe alle Absätze mit auf dem Inhaltsverzeichnisergebnis basierenden Stilen. Dies ist jeder Stil zwischen Inhaltsverzeichnis und Inhaltsverzeichnis9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Holen Sie sich den ersten Tabulator, der in diesem Absatz verwendet wird. Dies sollte der Tabulator sein, der zum Ausrichten der Seitenzahlen verwendet wird.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Ersetzen Sie den ersten Standard-Tabstopp durch einen benutzerdefinierten Tabstopp.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Siehe auch

* class [TabStop](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
