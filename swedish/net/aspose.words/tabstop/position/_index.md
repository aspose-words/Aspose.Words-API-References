---
title: TabStop.Position
linktitle: Position
articleTitle: Position
second_title: Aspose.Words för .NET
description: TabStop Position fast egendom. Får tabbstoppets position i poäng i C#.
type: docs
weight: 50
url: /sv/net/aspose.words/tabstop/position/
---
## TabStop.Position property

Får tabbstoppets position i poäng.

```csharp
public double Position { get; }
```

## Exempel

Visar hur man ändrar positionen för höger tabbstopp i innehållsförteckningsrelaterade stycken.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Iterera genom alla stycken med TOC resultatbaserade stilar; detta är vilken stil som helst mellan TOC och TOC9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Få den första fliken som används i det här stycket, detta bör vara den flik som används för att anpassa sidnumren.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Ersätt den första standardfliken, sluta med ett anpassat tabbstopp.
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### Se även

* class [TabStop](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
