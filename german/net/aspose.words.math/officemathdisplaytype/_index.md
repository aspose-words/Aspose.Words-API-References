---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words für .NET
description: Aspose.Words.Math.OfficeMathDisplayType opsomming. Gibt den Anzeigeformattyp der Gleichung an in C#.
type: docs
weight: 4130
url: /de/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

Gibt den Anzeigeformattyp der Gleichung an.

```csharp
public enum OfficeMathDisplayType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Display | `0` | Die Office Math wird in einer eigenen Zeile angezeigt. |
| Inline | `1` | Die Office Math wird inline mit dem Text angezeigt. |

## Beispiele

Zeigt, wie die Anzeigeformatierung für Office-Mathematik festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath-Knoten, die anderen OfficeMath-Knoten untergeordnet sind, sind immer inline.
// Der Knoten, mit dem wir arbeiten, ist der Basisknoten, um seinen Standort und Anzeigetyp zu ändern.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Ändern Sie den Speicherort und den Anzeigetyp des OfficeMath-Knotens.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Math](../../aspose.words.math/)
* Montage [Aspose.Words](../../)
