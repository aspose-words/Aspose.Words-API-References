---
title: LoadOptions.ConvertShapeToOfficeMath
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. EquationXML ile şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar.
type: docs
weight: 40
url: /tr/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

EquationXML ile şekillerin Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

### Örnekler

EquationXML şekillerinin Office Math nesnelerine nasıl dönüştürüleceğini gösterir.

```csharp
LoadOptions loadOptions = new LoadOptions();

// Şekillerin EquationXML nitelikleriyle dönüştürülüp dönüştürülmeyeceğini belirtmek için bu bayrağı kullanın
// Office Math nesnelerine ve ardından belgeyi yükleyin.
loadOptions.ConvertShapeToOfficeMath = isConvertShapeToOfficeMath;

Document doc = new Document(MyDir + "Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    Assert.AreEqual(16, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(34, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
else
{
    Assert.AreEqual(24, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(0, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


