---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words für .NET
description: Entdecken Sie die OfficeMath ParentParagraph-Eigenschaft, um einfach auf den übergeordneten Absatz eines beliebigen Knotens zuzugreifen und so die Formatierung und Struktur Ihres Dokuments zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Ruft das übergeordnete Element ab[`Paragraph`](../../../aspose.words/paragraph/) dieses Knotens.

```csharp
public Paragraph ParentParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../../aspose.words.math/)
* Montage [Aspose.Words](../../../)
