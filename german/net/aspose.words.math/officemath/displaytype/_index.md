---
title: OfficeMath.DisplayType
second_title: Aspose.Words für .NET-API-Referenz
description: OfficeMath eigendom. Ruft/legt den Anzeigeformattyp von Office Math ab der angibt ob eine Gleichung inline mit dem Text oder in einer eigenen Zeile angezeigt wird.
type: docs
weight: 10
url: /de/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Ruft/legt den Anzeigeformattyp von Office Math ab, der angibt, ob eine Gleichung inline mit dem Text oder in einer eigenen Zeile angezeigt wird.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

### Bemerkungen

Der Anzeigeformattyp wirkt sich nur auf die oberste Ebene von Office Math aus.

Der zurückgegebene Anzeigeformattyp ist immerInline für verschachteltes Office Math.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../officemath/)
* Montage [Aspose.Words](../../../)


