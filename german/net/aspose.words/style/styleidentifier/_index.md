---
title: Style.StyleIdentifier
second_title: Aspose.Words für .NET-API-Referenz
description: Style eigendom. Ruft die vom Gebietsschema unabhängige Stilkennung für einen integrierten Stil ab.
type: docs
weight: 160
url: /de/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

Ruft die vom Gebietsschema unabhängige Stilkennung für einen integrierten Stil ab.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

### Bemerkungen

Für benutzerdefinierte (benutzerdefinierte) Stile wird diese Eigenschaft zurückgegebenUser.

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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Style](../)
* namensraum [Aspose.Words](../../style/)
* Montage [Aspose.Words](../../../)


