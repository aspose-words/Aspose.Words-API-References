---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words für .NET
description: Aspose.Words.Math.OfficeMathJustification opsomming. Gibt die Begründung der Gleichung an in C#.
type: docs
weight: 4140
url: /de/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Gibt die Begründung der Gleichung an.

```csharp
public enum OfficeMathJustification
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| CenterGroup | `1` | Richtet Instanzen mathematischen Textes links relativ zueinander aus und zentriert die Gruppe mathematischer Texte (den mathematischen Absatz) relativ zur Seite. |
| Center | `2` | Zentriert jede Instanz eines mathematischen Textes einzeln in Bezug auf die Ränder. |
| Left | `3` | Linke Ausrichtung des mathematischen Absatzes. |
| Right | `4` | Richtige Begründung des mathematischen Absatzes. |
| Inline | `7` | Inline-Position von Math. |
| Default | `1` | StandardwertCenterGroup . |

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

* namensraum [Aspose.Words.Math](../../aspose.words.math/)
* Montage [Aspose.Words](../../)
