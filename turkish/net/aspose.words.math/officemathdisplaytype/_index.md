---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: .NET için Aspose.Words
description: Gelişmiş belge netliği ve sunumu için denklem görüntüleme biçimlerini kolayca özelleştirmek üzere Aspose.Words.Math.OfficeMathDisplayType enum'unu keşfedin.
type: docs
weight: 4820
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
| Display | `0` | Office Matematiği kendi satırında görüntülenir. |
| Inline | `1` | Office Math, metinle birlikte satır içi olarak görüntülenir. |

## Örnekler

Ofis matematik görüntüleme biçimlendirmesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Diğer OfficeMath düğümlerinin çocuğu olan OfficeMath düğümleri her zaman satır içidir.
// Üzerinde çalıştığımız düğüm, konumunu ve görüntüleme türünü değiştirecek temel düğümdür.
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
