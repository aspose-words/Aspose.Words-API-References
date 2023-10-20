---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words for .NET
description: OfficeMath DisplayType mülk. Bir denklemin text ile satır içi olarak mı yoksa kendi satırında mı görüntüleneceğini temsil eden Office Math görüntüleme biçimi türünü alır/ayarlar C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Bir denklemin text ile satır içi olarak mı yoksa kendi satırında mı görüntüleneceğini temsil eden Office Math görüntüleme biçimi türünü alır/ayarlar.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## Notlar

Görüntüleme biçimi türü yalnızca üst düzey Office Math için etkilidir.

Döndürülen görüntü formatı türü her zamanInline iç içe geçmiş Office Math için.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../../aspose.words.math/)
* toplantı [Aspose.Words](../../../)
