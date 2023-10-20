---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words für .NET
description: OfficeMath DisplayType eigendom. Ruft den Office MathAnzeigeformattyp ab bzw. legt ihn fest der angibt ob eine Gleichung inline mit dem Text oder in einer eigenen Zeile angezeigt wird in C#.
type: docs
weight: 10
url: /de/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Ruft den Office Math-Anzeigeformattyp ab bzw. legt ihn fest, der angibt, ob eine Gleichung inline mit dem Text oder in einer eigenen Zeile angezeigt wird.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## Bemerkungen

Der Anzeigeformattyp ist nur für Office Math der obersten Ebene wirksam.

Der zurückgegebene Anzeigeformattyp ist immerInline für verschachtelte Office Math.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../../aspose.words.math/)
* Montage [Aspose.Words](../../../)
