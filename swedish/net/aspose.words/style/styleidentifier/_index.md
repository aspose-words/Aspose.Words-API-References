---
title: Style.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words för .NET
description: Style StyleIdentifier fast egendom. Hämtar den lokala stilidentifieraren för en inbyggd stil i C#.
type: docs
weight: 150
url: /sv/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

Hämtar den lokala stilidentifieraren för en inbyggd stil.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

## Anmärkningar

För användardefinierade (anpassade) stilar returneras den här egenskapenUser.

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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Style](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
