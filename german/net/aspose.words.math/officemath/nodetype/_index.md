---
title: OfficeMath.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words für .NET
description: Entdecken Sie die OfficeMath NodeType-Eigenschaft, die effizient OfficeMath-Elemente zurückgibt und so die mathematischen Fähigkeiten Ihres Dokuments verbessert.
type: docs
weight: 40
url: /de/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

RückgabenOfficeMath .

```csharp
public override NodeType NodeType { get; }
```

## Beispiele

Zeigt, wie die Anzeigeformatierung für Office-Mathematik festgelegt wird.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath-Knoten, die untergeordnete Knoten anderer OfficeMath-Knoten sind, sind immer inline.
// Der Knoten, mit dem wir arbeiten, ist der Basisknoten, dessen Standort und Anzeigetyp wir ändern möchten.
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
* namensraum [Aspose.Words.Math](../../../aspose.words.math/)
* Montage [Aspose.Words](../../../)
