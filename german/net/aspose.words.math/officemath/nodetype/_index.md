---
title: OfficeMath.NodeType
second_title: Aspose.Words für .NET-API-Referenz
description: OfficeMath eigendom. Gibt zurückOfficeMath .
type: docs
weight: 40
url: /de/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

Gibt zurückOfficeMath .

```csharp
public override NodeType NodeType { get; }
```

### Beispiele

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../officemath/)
* Montage [Aspose.Words](../../../)


