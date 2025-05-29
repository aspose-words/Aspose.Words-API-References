---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: .NET için Aspose.Words
description: Office Math hizalamanızı kolayca özelleştirmek ve ayarlamak için OfficeMath Justification özelliğini keşfedin. Belgenizin sunumunu zahmetsizce geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Office Math gerekçesini alır/ayarlar.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## Notlar

Gerekçelendirme, Office Math görüntüleme biçimi türüne ayarlanamazInline.

Satır içi hizalama, Office Math görüntüleme biçimi türüne ayarlanamazDisplay.

Karşılık gelen[`DisplayType`](../displaytype/) Office Math gerekçelendirmesi ayarlanmadan önce ayarlanması gerekir.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../../aspose.words.math/)
* toplantı [Aspose.Words](../../../)
