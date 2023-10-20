---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words لـ .NET
description: OfficeMath DisplayType ملكية. الحصول على/تعيين نوع تنسيق عرض Office Math الذي يمثل ما إذا كانت المعادلة معروضة سطريًا مع text أو معروضة على السطر الخاص بها في C#.
type: docs
weight: 10
url: /ar/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

الحصول على/تعيين نوع تنسيق عرض Office Math الذي يمثل ما إذا كانت المعادلة معروضة سطريًا مع text أو معروضة على السطر الخاص بها.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## ملاحظات

يؤثر نوع تنسيق العرض على المستوى الأعلى من Office Math فقط.

نوع تنسيق العرض الذي تم إرجاعه هو دائمًاInline لمكتب الرياضيات المتداخلة.

## أمثلة

يوضح كيفية ضبط تنسيق عرض الرياضيات المكتبية.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// عقد OfficeMath التابعة لعقد OfficeMath الأخرى تكون دائمًا مضمّنة.
// العقدة التي نعمل معها هي العقدة الأساسية لتغيير موقعها ونوع العرض.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// تغيير الموقع ونوع العرض لعقدة OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### أنظر أيضا

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../../aspose.words.math/)
* المجسم [Aspose.Words](../../../)
