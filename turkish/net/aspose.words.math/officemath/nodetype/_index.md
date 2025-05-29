---
title: OfficeMath.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: .NET için Aspose.Words
description: Belgenizin matematiksel yeteneklerini geliştirerek OfficeMath öğelerini verimli bir şekilde döndüren OfficeMath NodeType özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

Geri DöndürürOfficeMath .

```csharp
public override NodeType NodeType { get; }
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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../../aspose.words.math/)
* toplantı [Aspose.Words](../../../)
