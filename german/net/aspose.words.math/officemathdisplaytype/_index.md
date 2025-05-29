---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Math.OfficeMathDisplayType, um die Anzeigeformate von Gleichungen einfach anzupassen und so die Übersichtlichkeit und Präsentation von Dokumenten zu verbessern.
type: docs
weight: 4820
url: /de/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

Gibt den Anzeigeformattyp der Gleichung an.

```csharp
public enum OfficeMathDisplayType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Display | `0` | Die Office-Mathematik wird in einer eigenen Zeile angezeigt. |
| Inline | `1` | Die Office-Mathematik wird in den Text eingebettet angezeigt. |

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

* namensraum [Aspose.Words.Math](../../aspose.words.math/)
* Montage [Aspose.Words](../../)
