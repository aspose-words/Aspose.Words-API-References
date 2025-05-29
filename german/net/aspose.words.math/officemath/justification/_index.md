---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words für .NET
description: Entdecken Sie die OfficeMath-Ausrichtungseigenschaft, um Ihre Office Math-Ausrichtung einfach anzupassen und festzulegen. Verbessern Sie mühelos die Präsentation Ihres Dokuments!
type: docs
weight: 20
url: /de/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Ruft die Office Math-Ausrichtung ab/legt sie fest.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## Bemerkungen

Die Ausrichtung kann nicht auf Office Math mit Anzeigeformattyp eingestellt werdenInline.

Die Inline-Ausrichtung kann nicht auf Office Math mit Anzeigeformattyp eingestellt werden.Display.

Entsprechend[`DisplayType`](../displaytype/) muss vor dem Festlegen der Office Math-Ausrichtung festgelegt werden.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* namensraum [Aspose.Words.Math](../../../aspose.words.math/)
* Montage [Aspose.Words](../../../)
