---
title: TabAlignment Enum
linktitle: TabAlignment
articleTitle: TabAlignment
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.TabAlignment enum for customizable tab stop alignment. Enhance document formatting with precision and flexibility today!
type: docs
weight: 7030
url: /net/aspose.words/tabalignment/
---
## TabAlignment enumeration

Specifies the alignment/type of a tab stop.

```csharp
public enum TabAlignment
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Left | `0` | Left-aligns the text after the tab stop. |
| Center | `1` | Centers the text around the tab stop. |
| Right | `2` | Right-aligns the text at the tab stop. |
| Decimal | `3` | Aligns the text at the decimal dot. |
| Bar | `4` | Draws a vertical bar at the tab stop position. |
| List | `6` | The tab is a delimiter between the number/bullet and text in a list item. |
| Clear | `7` | Clears any tab stop in this position. |

## Examples

Shows how to set custom tab stops for a paragraph.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// If we are in a paragraph with no tab stops in this collection,
// the cursor will jump 36 points each time we press the Tab key in Microsoft Word.
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// We can add custom tab stops in Microsoft Word if we enable the ruler via the "View" tab.
// Each unit on this ruler is two default tab stops, which is 72 points.
// We can add custom tab stops programmatically like this.
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// We can see these tab stops in Microsoft Word by enabling the ruler via "View" -> "Show" -> "Ruler".
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// Any tab characters we add will make use of the tab stops on the ruler and may,
// depending on the tab leader's value, leave a line between the tab departure and arrival destinations.
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### See Also

* namespace [Aspose.Words](../../aspose.words/)
* assembly [Aspose.Words](../../)
