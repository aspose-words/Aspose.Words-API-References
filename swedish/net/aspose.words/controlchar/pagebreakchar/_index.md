---
title: ControlChar.PageBreakChar
linktitle: PageBreakChar
articleTitle: PageBreakChar
second_title: Aspose.Words för .NET
description: Upptäck fältet ControlChar PageBreakChar för effektiv dokumentformatering. Förbättra ditt arbetsflöde med anpassningsbara sidbrytningsalternativ!
type: docs
weight: 210
url: /sv/net/aspose.words/controlchar/pagebreakchar/
---
## ControlChar.PageBreakChar field

Sidbrytningstecken: (char)12 eller "\f".

```csharp
public const char PageBreakChar;
```

## Exempel

Visar hur man lägger till olika kontrolltecken i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Lägg till ett vanligt mellanslag.
builder.Write("Before space." + ControlChar.SpaceChar + "After space.");

// Lägg till ett NBSP, vilket är ett fast mellanslag.
// Till skillnad från det vanliga mellanrummet kan detta mellanrum inte ha en automatisk radbrytning på sin position.
builder.Write("Before space." + ControlChar.NonBreakingSpace + "After space.");

// Lägg till ett tabbtecken.
builder.Write("Before tab." + ControlChar.Tab + "After tab.");

// Lägg till en radbrytning.
builder.Write("Before line break." + ControlChar.LineBreak + "After line break.");

// Lägger till en ny rad och börjar ett nytt stycke.
Assert.AreEqual(1, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);
builder.Write("Before line feed." + ControlChar.LineFeed + "After line feed.");
Assert.AreEqual(2, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Radmatningstecknet har två versioner.
Assert.AreEqual(ControlChar.LineFeed, ControlChar.Lf);

// Vagnreturer och radmatningar kan representeras tillsammans med ett tecken.
Assert.AreEqual(ControlChar.CrLf, ControlChar.Cr + ControlChar.Lf);

// Lägg till en styckebrytning, vilket startar ett nytt stycke.
builder.Write("Before paragraph break." + ControlChar.ParagraphBreak + "After paragraph break.");
Assert.AreEqual(3, doc.FirstSection.Body.GetChildNodes(NodeType.Paragraph, true).Count);

// Lägg till en avsnittsbrytning. Detta skapar inte ett nytt avsnitt eller stycke.
Assert.AreEqual(1, doc.Sections.Count);
builder.Write("Before section break." + ControlChar.SectionBreak + "After section break.");
Assert.AreEqual(1, doc.Sections.Count);

// Lägg till en sidbrytning.
builder.Write("Before page break." + ControlChar.PageBreak + "After page break.");

// En sidbrytning har samma värde som en avsnittsbrytning.
Assert.AreEqual(ControlChar.PageBreak, ControlChar.SectionBreak);

// Infoga ett nytt avsnitt och sätt sedan kolumnantalet till två.
doc.AppendChild(new Section(doc));
builder.MoveToSection(1);
builder.CurrentSection.PageSetup.TextColumns.SetCount(2);

// Vi kan använda ett kontrolltecken för att markera punkten där texten flyttas till nästa kolumn.
builder.Write("Text at end of column 1." + ControlChar.ColumnBreak + "Text at beginning of column 2.");

doc.Save(ArtifactsDir + "ControlChar.InsertControlChars.docx");

// Det finns motsvarigheter för tecken och strängar för de flesta tecken.
Assert.AreEqual(Convert.ToChar(ControlChar.Cell), ControlChar.CellChar);
Assert.AreEqual(Convert.ToChar(ControlChar.NonBreakingSpace), ControlChar.NonBreakingSpaceChar);
Assert.AreEqual(Convert.ToChar(ControlChar.Tab), ControlChar.TabChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineBreak), ControlChar.LineBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.LineFeed), ControlChar.LineFeedChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ParagraphBreak), ControlChar.ParagraphBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.SectionBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.PageBreak), ControlChar.SectionBreakChar);
Assert.AreEqual(Convert.ToChar(ControlChar.ColumnBreak), ControlChar.ColumnBreakChar);
```

### Se även

* class [ControlChar](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
