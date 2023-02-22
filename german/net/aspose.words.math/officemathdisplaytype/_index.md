---
title: Enum OfficeMathDisplayType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Math.OfficeMathDisplayType opsomming. Gibt den Anzeigeformattyp der Gleichung an.
type: docs
weight: 3890
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
| Display | `0` | Office Math wird in einer eigenen Zeile angezeigt. |
| Inline | `1` | Office Math wird inline mit dem Text angezeigt. |

### Beispiele

Zeigt, wie die Anzeigeformatierung für Office-Mathematik eingestellt wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath-Knoten, die Kinder anderer OfficeMath-Knoten sind, sind immer inline.
// Der Knoten, mit dem wir arbeiten, ist der Basisknoten, um seine Position und seinen Anzeigetyp zu ändern.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// OOXML- und WML-Formate verwenden die Eigenschaft "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Position und Anzeigetyp des OfficeMath-Knotens ändern.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Siehe auch

* namensraum [Aspose.Words.Math](../../aspose.words.math/)
* Montage [Aspose.Words](../../)


