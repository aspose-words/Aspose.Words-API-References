---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: .NET için Aspose.Words
description: Hassas denklem hizalaması için Aspose.Words.Math.OfficeMathJustification enum'unu keşfedin. Belgenizin netliğini en uygun hizalama seçenekleriyle artırın.
type: docs
weight: 4830
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
| CenterGroup | `1` | Matematiksel metin örneklerini birbirlerine göre sola yaslar ve matematiksel metin grubunu (Matematik Paragrafı) sayfaya göre ortalar. |
| Center | `2` | Matematiksel metnin her örneğini kenar boşluklarına göre ayrı ayrı ortalar. |
| Left | `3` | Matematik Paragrafının sol hizalaması. |
| Right | `4` | Matematik Paragrafının Sağa Yaslanması. |
| Inline | `7` | Math. 'nin satır içi konumu |
| Default | `1` | Varsayılan değerCenterGroup . |

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
