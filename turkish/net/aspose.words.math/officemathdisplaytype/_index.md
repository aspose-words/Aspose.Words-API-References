---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words for .NET
description: Aspose.Words.Math.OfficeMathDisplayType Sıralama. Denklemin görüntüleme biçimi türünü belirtir C#'da.
type: docs
weight: 4130
url: /tr/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

Denklemin görüntüleme biçimi türünü belirtir.

```csharp
public enum OfficeMathDisplayType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Display | `0` | Office Math kendi satırında görüntülenir. |
| Inline | `1` | Office Math, metinle aynı satırda görüntülenir. |

## Örnekler

Ofis matematik ekranı formatının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Diğer OfficeMath düğümlerinin çocukları olan OfficeMath düğümleri her zaman satır içidir.
// Çalıştığımız düğüm, konumunu ve görüntüleme türünü değiştirecek temel düğümdür.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// OfficeMath düğümünün konumunu ve görüntüleme türünü değiştirin.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Math](../../aspose.words.math/)
* toplantı [Aspose.Words](../../)
