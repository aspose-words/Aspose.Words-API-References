---
title: OfficeMath.EquationXmlEncoding
second_title: Aspose.Words für .NET-API-Referenz
description: OfficeMath eigendom. Ruft/legt eine Kodierung ab die verwendet wurde um GleichungsXML zu kodieren wenn dieses OfficeMathematikobjekt aus GleichungsXML gelesen wird. Wir verwenden die Codierung beim Speichern eines Dokuments um in derselben Codierung zu schreiben in der es gelesen wurde.
type: docs
weight: 20
url: /de/net/aspose.words.math/officemath/equationxmlencoding/
---
## OfficeMath.EquationXmlEncoding property

Ruft/legt eine Kodierung ab, die verwendet wurde, um Gleichungs-XML zu kodieren, wenn dieses Office-Mathematikobjekt aus Gleichungs-XML gelesen wird. Wir verwenden die Codierung beim Speichern eines Dokuments, um in derselben Codierung zu schreiben, in der es gelesen wurde.

```csharp
public Encoding EquationXmlEncoding { get; set; }
```

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

* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../officemath/)
* Montage [Aspose.Words](../../../)


