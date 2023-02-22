---
title: TabStop.Position
second_title: Aspose.Words für .NET-API-Referenz
description: TabStop eigendom. Ruft die Position des Tabstopps in Punkten ab.
type: docs
weight: 50
url: /de/net/aspose.words/tabstop/position/
---
## TabStop.Position property

Ruft die Position des Tabstopps in Punkten ab.

```csharp
public double Position { get; }
```

### Beispiele

Zeigt, wie die Position des rechten Tabstopps in TOC-bezogenen Absätzen geändert wird.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Durch alle Absätze mit TOC-ergebnisbasierten Stilen iterieren; dies ist ein beliebiger Stil zwischen TOC und TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Holen Sie sich den ersten in diesem Absatz verwendeten Tabulator, dies sollte der Tabulator sein, der zum Ausrichten der Seitenzahlen verwendet wird.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Ersetzen Sie den ersten Standard-Tabstopp durch einen benutzerdefinierten Tabstopp.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Siehe auch

* class [TabStop](../)
* namensraum [Aspose.Words](../../tabstop/)
* Montage [Aspose.Words](../../../)


