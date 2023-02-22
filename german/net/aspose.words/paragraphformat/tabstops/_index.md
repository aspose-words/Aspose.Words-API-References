---
title: ParagraphFormat.TabStops
second_title: Aspose.Words für .NET-API-Referenz
description: ParagraphFormat eigendom. Ruft die Sammlung benutzerdefinierter Tabstopps ab die für dieses Objekt definiert sind.
type: docs
weight: 380
url: /de/net/aspose.words/paragraphformat/tabstops/
---
## ParagraphFormat.TabStops property

Ruft die Sammlung benutzerdefinierter Tabstopps ab, die für dieses Objekt definiert sind.

```csharp
public TabStopCollection TabStops { get; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [ParagraphFormat](../)
* namensraum [Aspose.Words](../../paragraphformat/)
* Montage [Aspose.Words](../../../)


