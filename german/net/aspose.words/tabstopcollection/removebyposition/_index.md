---
title: TabStopCollection.RemoveByPosition
second_title: Aspose.Words für .NET-API-Referenz
description: TabStopCollection methode. Entfernt einen Tabstopp an der angegebenen Position aus der Sammlung.
type: docs
weight: 120
url: /de/net/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection.RemoveByPosition method

Entfernt einen Tabstopp an der angegebenen Position aus der Sammlung.

```csharp
public void RemoveByPosition(double position)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| position | Double | Die Position (in Punkt) des zu entfernenden Tabstopps. |

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

* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../tabstopcollection/)
* Montage [Aspose.Words](../../../)


