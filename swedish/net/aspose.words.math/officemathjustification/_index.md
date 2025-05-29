---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Math.OfficeMathJustification-enum för exakt ekvationsjustering. Förbättra dokumentets tydlighet med optimala justeringsalternativ.
type: docs
weight: 4830
url: /sv/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Anger ekvationens justering.

```csharp
public enum OfficeMathJustification
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| CenterGroup | `1` | Justerar förekomster av matematisk text till vänster i förhållande till varandra och centrerar gruppen av matematisk text (matematikstycket) i förhållande till sidan. |
| Center | `2` | Centrerar varje förekomst av matematisk text individuellt med avseende på marginaler. |
| Left | `3` | Vänsterjustering av matematiskt stycke. |
| Right | `4` | Högerjustering av matematiskt stycke. |
| Inline | `7` | Inline-position för Math. |
| Default | `1` | StandardvärdeCenterGroup . |

## Exempel

Visar hur man ställer in formatering för Office-matematikvisning.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath-noder som är underordnade till andra OfficeMath-noder är alltid inline.
// Noden vi arbetar med är basnoden för att ändra dess plats och visningstyp.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Ändra plats och visningstyp för OfficeMath-noden.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Se även

* namnutrymme [Aspose.Words.Math](../../aspose.words.math/)
* hopsättning [Aspose.Words](../../)
