---
title: OfficeMath.ParentParagraph
second_title: Aspose.Words for .NET API Referansı
description: OfficeMath mülk. Üst öğeyi alırParagraph bu düğümün.
type: docs
weight: 60
url: /tr/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Üst öğeyi alır[`Paragraph`](../../../aspose.words/paragraph/) bu düğümün.

```csharp
public Paragraph ParentParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../officemath/)
* toplantı [Aspose.Words](../../../)


