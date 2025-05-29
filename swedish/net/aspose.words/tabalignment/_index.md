---
title: TabAlignment Enum
linktitle: TabAlignment
articleTitle: TabAlignment
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.TabAlignment-enum för anpassningsbar tabbstoppsjustering. Förbättra dokumentformateringen med precision och flexibilitet idag!
type: docs
weight: 7030
url: /sv/net/aspose.words/tabalignment/
---
## TabAlignment enumeration

Anger justeringen/typen för ett tabbstopp.

```csharp
public enum TabAlignment
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Left | `0` | Vänsterjusterar texten efter tabbstoppet. |
| Center | `1` | Centrerar texten runt tabbstoppet. |
| Right | `2` | Högerjusterar texten vid tabbstoppet. |
| Decimal | `3` | Justerar texten vid decimalpunkten. |
| Bar | `4` | Ritar en vertikal streckpunkt vid tabbstoppspositionen. |
| List | `6` | Tabben är en avgränsare mellan numret/punkten och texten i ett listobjekt. |
| Clear | `7` | Rensar alla tabbstopp i den här positionen. |

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
