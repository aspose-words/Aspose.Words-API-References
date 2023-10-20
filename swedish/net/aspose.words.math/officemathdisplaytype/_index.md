---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words för .NET
description: Aspose.Words.Math.OfficeMathDisplayType uppräkning. Anger visningsformattypen för ekvationen i C#.
type: docs
weight: 4130
url: /sv/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

Anger visningsformattypen för ekvationen.

```csharp
public enum OfficeMathDisplayType
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Display | `0` | Office Math visas på sin egen rad. |
| Inline | `1` | Office Math visas i linje med texten. |

## Exempel

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
