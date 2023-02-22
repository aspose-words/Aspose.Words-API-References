---
title: Enum OfficeMathJustification
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Math.OfficeMathJustification opsomming. Gibt die Begründung der Gleichung an.
type: docs
weight: 3900
url: /de/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Gibt die Begründung der Gleichung an.

```csharp
public enum OfficeMathJustification
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| CenterGroup | `1` | Richtet Instanzen von mathematischem Text linksbündig zueinander aus und zentriert die Gruppe von mathematischem Text (der mathematische Absatz) in Bezug auf die Seite. |
| Center | `2` | Zentriert jede Instanz von mathematischem Text einzeln in Bezug auf die Ränder. |
| Left | `3` | Linke Ausrichtung des mathematischen Absatzes. |
| Right | `4` | Rechte Ausrichtung des mathematischen Absatzes. |
| Inline | `7` | Inline-Position von Math. |
| Default | `1` | StandardwertCenterGroup . |

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


