---
title: TabLeader Enum
linktitle: TabLeader
articleTitle: TabLeader
second_title: Aspose.Words for .NET
description: Aspose.Words.TabLeader enum. Specifies the type of the leader line displayed under the tab character in C#.
type: docs
weight: 6550
url: /net/aspose.words/tableader/
---
## TabLeader enumeration

Specifies the type of the leader line displayed under the tab character.

```csharp
public enum TabLeader
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | No leader line is displayed. |
| Dots | `1` | The leader line is made up from dots. |
| Dashes | `2` | The leader line is made up from dashes. |
| Line | `3` | The leader line is a single line. |
| Heavy | `4` | The leader line is a single thick line. |
| MiddleDot | `5` | The leader line is made up from middle-dots. |

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
