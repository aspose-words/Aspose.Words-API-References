---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words for .NET
description: OfficeMath Justification mülk. Office Matematik gerekçesini alır/ayarlar C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Office Matematik gerekçesini alır/ayarlar.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## Notlar

Gerekçe, görüntüleme biçimi türüyle Office Math'a ayarlanamazInline.

Satır içi yaslama, görüntüleme biçimi türüyle Office Math'a ayarlanamazDisplay.

karşılık gelen[`DisplayType`](../displaytype/) Office Math gerekçesini ayarlamadan önce ayarlanması gerekir.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../../aspose.words.math/)
* toplantı [Aspose.Words](../../../)
