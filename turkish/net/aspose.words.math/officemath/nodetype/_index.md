---
title: OfficeMath.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words for .NET
description: OfficeMath NodeType mülk. İadelerOfficeMath  C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

İadelerOfficeMath .

```csharp
public override NodeType NodeType { get; }
```

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* ad alanı [Aspose.Words.Math](../../../aspose.words.math/)
* toplantı [Aspose.Words](../../../)
