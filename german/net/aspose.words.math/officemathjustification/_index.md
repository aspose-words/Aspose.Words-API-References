---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.Math.OfficeMathJustification für die präzise Ausrichtung von Gleichungen. Verbessern Sie die Übersichtlichkeit Ihres Dokuments mit optimalen Ausrichtungsoptionen.
type: docs
weight: 4830
url: /de/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Gibt die Ausrichtung der Gleichung an.

```csharp
public enum OfficeMathJustification
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| CenterGroup | `1` | Richtet mathematischen Text linksbündig zueinander aus und zentriert die Gruppe mathematischen Textes (den Mathematik-Absatz) in Bezug auf die Seite. |
| Center | `2` | Zentriert jede Instanz mathematischen Textes einzeln hinsichtlich der Ränder. |
| Left | `3` | Linksbündiger Mathe-Absatz. |
| Right | `4` | Rechtsbündiger Mathematik-Absatz. |
| Inline | `7` | Inline-Position von Math. |
| Default | `1` | StandardwertCenterGroup . |

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
