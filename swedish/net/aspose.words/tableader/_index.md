---
title: TabLeader Enum
linktitle: TabLeader
articleTitle: TabLeader
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.TabLeader-enumerationen, som definierar hänvisningslinjer för tabbar, förbättrar dokumentformatering och läsbarhet i dina projekt.
type: docs
weight: 7040
url: /sv/net/aspose.words/tableader/
---
## TabLeader enumeration

Anger typen av hänvisningslinje som visas under tabbtecknet.

```csharp
public enum TabLeader
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Ingen hänvisningslinje visas. |
| Dots | `1` | Linjelinjen består av punkter. |
| Dashes | `2` | Linjelinjen består av bindestreck. |
| Line | `3` | Inledningslinjen är en enda linje. |
| Heavy | `4` | Riktlinjen är en enda tjock linje. |
| MiddleDot | `5` | Topplinjen består av mittpunkter. |

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

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
