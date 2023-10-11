---
title: OfficeMath.ParentParagraph
second_title: Aspose.Words für .NET-API-Referenz
description: OfficeMath eigendom. Ruft das übergeordnete Element abParagraph dieses Knotens.
type: docs
weight: 50
url: /de/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Ruft das übergeordnete Element ab[`Paragraph`](../../../aspose.words/paragraph/) dieses Knotens.

```csharp
public Paragraph ParentParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../officemath/)
* Montage [Aspose.Words](../../../)


