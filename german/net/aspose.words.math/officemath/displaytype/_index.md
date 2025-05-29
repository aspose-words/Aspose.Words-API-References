---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words für .NET
description: Entdecken Sie die OfficeMath DisplayType-Eigenschaft für eine flexible Formelformatierung – wählen Sie zwischen Inline- oder Standalone-Anzeige für eine verbesserte Dokumentübersichtlichkeit.
type: docs
weight: 10
url: /de/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Ruft den Office Math-Anzeigeformattyp ab/legt ihn fest, der angibt, ob eine Gleichung in den Text oder in einer eigenen Zeile angezeigt wird.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## Bemerkungen

Der Anzeigeformattyp wirkt sich nur auf Office Math der obersten Ebene aus.

Der zurückgegebene Anzeigeformattyp ist immerInline für verschachtelte Office-Mathematik.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../../aspose.words.math/)
* Montage [Aspose.Words](../../../)
