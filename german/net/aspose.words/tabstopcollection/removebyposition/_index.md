---
title: TabStopCollection.RemoveByPosition
linktitle: RemoveByPosition
articleTitle: RemoveByPosition
second_title: Aspose.Words für .NET
description: Entfernen Sie Tabstopps mühelos aus Ihrer Sammlung mit der Methode „RemoveByPosition“. Optimieren Sie Ihre Formatierung für eine bessere Dokumentenkontrolle!
type: docs
weight: 120
url: /de/net/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection.RemoveByPosition method

Entfernt einen Tabulator an der angegebenen Position aus der Auflistung.

```csharp
public void RemoveByPosition(double position)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| position | Double | Die Position (in Punkten) des zu entfernenden Tabulatorstopps. |

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

* class [TabStopCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
