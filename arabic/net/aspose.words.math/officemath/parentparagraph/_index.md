---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParentParagraph في OfficeMath للوصول بسهولة إلى الفقرة الأصلية لأي عقدة، مما يعمل على تحسين تنسيق مستندك وبنيته.
type: docs
weight: 50
url: /ar/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

يسترد الأصل[`Paragraph`](../../../aspose.words/paragraph/) من هذه العقدة.

```csharp
public Paragraph ParentParagraph { get; }
```

## أمثلة

يوضح كيفية تعيين تنسيق عرض الرياضيات في المكتب.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// عقد OfficeMath التي تعد أبناء لعقد OfficeMath الأخرى تكون دائمًا مضمنة.
// العقدة التي نعمل معها هي العقدة الأساسية لتغيير موقعها ونوع العرض.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// تغيير موقع ونوع العرض لعقدة OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### أنظر أيضا

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../../aspose.words.math/)
* المجسم [Aspose.Words](../../../)
