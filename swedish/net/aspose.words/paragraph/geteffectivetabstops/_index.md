---
title: Paragraph.GetEffectiveTabStops
linktitle: GetEffectiveTabStops
articleTitle: GetEffectiveTabStops
second_title: Aspose.Words för .NET
description: Upptäck metoden GetEffectiveTabStops för att hämta alla tabbstopp i ett stycke, inklusive de från formateringar och listor för förbättrad formatering.
type: docs
weight: 270
url: /sv/net/aspose.words/paragraph/geteffectivetabstops/
---
## Paragraph.GetEffectiveTabStops method

Returnerar en matris med alla tabbstopp som tillämpats på detta stycke, inklusive indirekt tillämpade av format eller listor.

```csharp
public TabStop[] GetEffectiveTabStops()
```

## Exempel

Visar hur man ställer in anpassade tabbstopp för ett stycke.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// Om vi är i ett stycke utan tabbstopp i den här samlingen,
// markören hoppar 36 punkter varje gång vi trycker på Tab-tangenten i Microsoft Word.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// Vi kan lägga till anpassade tabbstopp i Microsoft Word om vi aktiverar linjalen via fliken "Visa".
// Varje enhet på denna linjal är två standardtabbstopp, vilket är 72 punkter.
// Vi kan lägga till anpassade tabbstopp programmatiskt så här.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// Vi kan se dessa tabbstopp i Microsoft Word genom att aktivera linjalen via "Visa" -> "Visa" -> "Linjal".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Alla tabbtecken vi lägger till kommer att använda tabbstoppen på linjalen och kan,
// beroende på flikhuvudets värde, lämna en rad mellan flikarnas avgångs- och ankomstdestinationer.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### Se även

* class [TabStop](../../tabstop/)
* class [Paragraph](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
