---
title: OfficeMath.EquationXmlEncoding
second_title: Aspose.Words for .NET API Referansı
description: OfficeMath mülk. Bu ofis matematik nesnesi denklem XMLsinden okunuyorsa denklem XMLsini kodlamak için kullanılan bir kodlamayı alır/ayarlar. Bir belgeyi okunduğu kodlamayla yazmak için kaydederken kodlamayı kullanırız.
type: docs
weight: 20
url: /tr/net/aspose.words.math/officemath/equationxmlencoding/
---
## OfficeMath.EquationXmlEncoding property

Bu ofis matematik nesnesi denklem XML'sinden okunuyorsa, denklem XML'sini kodlamak için kullanılan bir kodlamayı alır/ayarlar. Bir belgeyi, okunduğu kodlamayla yazmak için kaydederken kodlamayı kullanırız.

```csharp
public Encoding EquationXmlEncoding { get; set; }
```

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

* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../officemath/)
* toplantı [Aspose.Words](../../../)


