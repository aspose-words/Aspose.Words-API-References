---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية محاذاة OfficeMath لتخصيص وضبط محاذاة Office Math بسهولة. حسّن عرض مستندك بسهولة!
type: docs
weight: 20
url: /ar/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

يحصل على/يعين مبرر Office Math.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## ملاحظات

لا يمكن ضبط التبرير على Office Math مع نوع تنسيق العرضInline.

لا يمكن ضبط المحاذاة المضمنة على Office Math مع نوع تنسيق العرضDisplay.

مُتَجَانِس[`DisplayType`](../displaytype/) يجب تعيين ذلك قبل تعيين مبرر Office Math.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../../aspose.words.math/)
* المجسم [Aspose.Words](../../../)
