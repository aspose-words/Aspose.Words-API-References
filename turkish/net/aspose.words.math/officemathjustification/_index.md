---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words for .NET
description: Aspose.Words.Math.OfficeMathJustification Sıralama. Denklemin gerekçesini belirtir C#'da.
type: docs
weight: 4140
url: /tr/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Denklemin gerekçesini belirtir.

```csharp
public enum OfficeMathJustification
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| CenterGroup | `1` | Matematiksel metin örneklerini birbirine göre sola yaslar ve math metin grubunu (Matematik Paragrafı) sayfaya göre ortalar. |
| Center | `2` | Matematiksel metnin her örneğini kenar boşluklarına göre ayrı ayrı ortalar. |
| Left | `3` | Matematik Paragrafının sola yaslanması. |
| Right | `4` | Matematik Paragrafının Doğru Gerekçesi. |
| Inline | `7` | Math. 'nin satır içi konumu |
| Default | `1` | Varsayılan değerCenterGroup . |

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
