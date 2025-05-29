---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaften von TabStop Leader, um die Führungslinientypen für Ihre Tabs anzupassen und so die Übersichtlichkeit und Präsentation Ihres Dokuments zu verbessern. Optimieren Sie Ihre Formatierung noch heute!
type: docs
weight: 40
url: /de/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Ruft den Typ der unter dem Tabulatorzeichen angezeigten Führungslinie ab oder legt ihn fest.

```csharp
public TabLeader Leader { get; set; }
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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
