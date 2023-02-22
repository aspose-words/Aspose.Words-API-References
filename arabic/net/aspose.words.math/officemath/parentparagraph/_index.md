---
title: OfficeMath.ParentParagraph
second_title: Aspose.Words لمراجع .NET API
description: OfficeMath ملكية. استرداد الأصلParagraph من هذه العقدة.
type: docs
weight: 60
url: /ar/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

استرداد الأصل[`Paragraph`](../../../aspose.words/paragraph/) من هذه العقدة.

```csharp
public Paragraph ParentParagraph { get; }
```

### أمثلة

يوضح كيفية تعيين تنسيق عرض الرياضيات في المكتب.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// تكون عُقد OfficeMath التابعة لعقد OfficeMath الأخرى مضمنة دائمًا.
// العقدة التي نعمل معها هي العقدة الأساسية لتغيير موقعها ونوع عرضها.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// تستخدم تنسيقات OOXML و WML الخاصية "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// تغيير الموقع ونوع العرض لعقدة OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### أنظر أيضا

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../officemath/)
* المجسم [Aspose.Words](../../../)


