---
title: TabStop.Leader
second_title: Aspose.Words für .NET-API-Referenz
description: TabStop eigendom. Ruft den Typ der Führungslinie ab die unter dem Tabulatorzeichen angezeigt wird oder legt diesen fest.
type: docs
weight: 40
url: /de/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

Ruft den Typ der Führungslinie ab, die unter dem Tabulatorzeichen angezeigt wird, oder legt diesen fest.

```csharp
public TabLeader Leader { get; set; }
```

### Beispiele

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

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* namensraum [Aspose.Words](../../tabstop/)
* Montage [Aspose.Words](../../../)


