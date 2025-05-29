---
title: Style.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words für .NET
description: Entdecken Sie die lokal unabhängige StyleIdentifier-Eigenschaft für integrierte Stile. Optimieren Sie Ihre Projekte mit konsistenten und vielseitigen Styling-Lösungen.
type: docs
weight: 180
url: /de/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

Ruft die gebietsschemaunabhängige Stilkennung für einen integrierten Stil ab.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

## Bemerkungen

Für benutzerdefinierte Stile gibt diese Eigenschaft zurückUser.

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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Style](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
