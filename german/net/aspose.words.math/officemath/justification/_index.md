---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words für .NET
description: OfficeMath Justification eigendom. Ruft die Office MathBegründung ab bzw. legt sie fest in C#.
type: docs
weight: 20
url: /de/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Ruft die Office Math-Begründung ab bzw. legt sie fest.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## Bemerkungen

Die Ausrichtung kann nicht auf den Anzeigeformattyp „Office Math“ eingestellt werdenInline.

Die Inline-Ausrichtung kann nicht auf den Anzeigeformattyp „Office Math“ eingestellt werdenDisplay.

Dazugehörigen[`DisplayType`](../displaytype/) muss vor dem Festlegen der Office Math-Ausrichtung festgelegt werden.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../../aspose.words.math/)
* Montage [Aspose.Words](../../../)
