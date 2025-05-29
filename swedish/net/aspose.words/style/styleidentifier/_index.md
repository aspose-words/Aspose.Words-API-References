---
title: Style.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words för .NET
description: Upptäck den språkoberoende StyleIdentifier-egenskapen för inbyggda stilar. Förbättra dina projekt med konsekventa och mångsidiga stylinglösningar.
type: docs
weight: 180
url: /sv/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

Hämtar den språkoberoende stilidentifieraren för en inbyggd stil.

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

## Anmärkningar

För användardefinierade (anpassade) stilar returnerar den här egenskapenUser.

## Exempel

Visar hur man ändrar positionen för höger tabbstopp i stycken relaterade till innehållsförteckningen.

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// Iterera genom alla stycken med resultatbaserade stilar baserade på innehållsförteckningen; detta är vilken stil som helst mellan innehållsförteckning och innehållsförteckning9.
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // Hämta den första tabbtangenten som används i detta stycke, detta ska vara den tabbtangent som används för att justera sidnumren.
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // Ersätt den första standardtabbstoppet med en anpassad tabbstopp.
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
