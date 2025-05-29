---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: .NET için Aspose.Words
description: Herhangi bir düğümün üst Paragrafına kolayca erişmek, belge biçimlendirmenizi ve yapınızı geliştirmek için OfficeMath ParentParagraph özelliğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Üst öğeyi alır[`Paragraph`](../../../aspose.words/paragraph/) bu düğümün.

```csharp
public Paragraph ParentParagraph { get; }
```

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../../aspose.words.math/)
* toplantı [Aspose.Words](../../../)
