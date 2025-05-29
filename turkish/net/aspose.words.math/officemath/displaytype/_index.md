---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: .NET için Aspose.Words
description: Esnek denklem biçimlendirmesi için OfficeMath DisplayType özelliğini keşfedin; gelişmiş belge netliği için satır içi veya bağımsız görüntüleme arasında seçim yapın.
type: docs
weight: 10
url: /tr/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Bir denklemin metinle aynı satırda mı yoksa kendi satırında mı görüntüleneceğini temsil eden Office Math görüntüleme biçimi türünü alır/ayarlar.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## Notlar

Görüntüleme biçimi türü yalnızca en üst düzey Office Math için geçerlidir.

Döndürülen görüntüleme biçimi türü her zamanInline iç içe Office Math için.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../../aspose.words.math/)
* toplantı [Aspose.Words](../../../)
