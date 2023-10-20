---
title: TabStop.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words für .NET
description: TabStop Position eigendom. Ermittelt die Position des Tabstopps in Punkten in C#.
type: docs
weight: 50
url: /de/net/aspose.words/tabstop/position/
---
## TabStop.Position property

Ermittelt die Position des Tabstopps in Punkten.

```csharp
public double Position { get; }
```

## Beispiele

Zeigt, wie die Position des rechten Tabstopps in Inhaltsverzeichnis-bezogenen Absätzen geändert wird.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Alle Absätze mit TOC-ergebnisbasierten Stilen durchlaufen; Dies ist jeder Stil zwischen TOC und TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Holen Sie sich den ersten Tab, der in diesem Absatz verwendet wird. Dies sollte der Tab sein, der zum Ausrichten der Seitenzahlen verwendet wird.
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
