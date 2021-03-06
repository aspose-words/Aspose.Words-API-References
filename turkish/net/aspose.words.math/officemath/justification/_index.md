---
title: Justification
second_title: Aspose.Words for .NET API Referansı
description: Office Math gerekçesini alır/ayarlar.
type: docs
weight: 30
url: /tr/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Office Math gerekçesini alır/ayarlar.

```csharp
public OfficeMathJustification Justification { get; set; }
```

### Notlar

Gerekçe, görüntüleme biçimi türüyle Office Math'a ayarlanamazInline.

Satır içi yaslama, görüntüleme biçimi türüyle Office Math'a ayarlanamazDisplay.

karşılık gelen[`DisplayType`](../displaytype) Office Math gerekçesini ayarlamadan önce ayarlanmalıdır.

### Örnekler

Office matematik ekranı biçimlendirmesinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Diğer OfficeMath düğümlerinin çocukları olan OfficeMath düğümleri her zaman satır içidir.
// Çalıştığımız düğüm, konumunu ve görüntüleme türünü değiştirmek için temel düğümdür.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// OOXML ve WML biçimleri "EquationXmlEncoding" özelliğini kullanır.
Assert.IsNull(officeMath.EquationXmlEncoding);

// OfficeMath düğümünün konumunu ve görüntüleme türünü değiştirin.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Ayrıca bakınız

* enum [OfficeMathJustification](../../officemathjustification)
* class [OfficeMath](../../officemath)
* ad alanı [Aspose.Words.Math](../../officemath)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
