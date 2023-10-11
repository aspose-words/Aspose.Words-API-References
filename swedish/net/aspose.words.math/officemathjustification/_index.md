---
title: Enum OfficeMathJustification
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Math.OfficeMathJustification uppräkning. Anger motiveringen av ekvationen.
type: docs
weight: 4140
url: /sv/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Anger motiveringen av ekvationen.

```csharp
public enum OfficeMathJustification
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| CenterGroup | `1` | Justerar instanser av matematisk text till vänster i förhållande till varandra och centrerar gruppen matematisk text (Matematisk stycke) med avseende på sidan. |
| Center | `2` | Centrerar varje instans av matematisk text individuellt med avseende på marginaler. |
| Left | `3` | Vänster motivering av Math Paragraph. |
| Right | `4` | Rätt motivering av matematisk paragraf. |
| Inline | `7` | Inline position för Math. |
| Default | `1` | StandardvärdeCenterGroup . |

### Exempel

Visar hur du ställer in kontorsmattevisningsformatering.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath-noder som är barn till andra OfficeMath-noder är alltid inline.
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


