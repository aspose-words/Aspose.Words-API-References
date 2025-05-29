---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OfficeMath DisplayType لتنسيق المعادلات بشكل مرن - اختر بين العرض المضمن أو المستقل لتحسين وضوح المستند.
type: docs
weight: 10
url: /ar/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

يحصل على/يعين نوع تنسيق عرض Office Math الذي يمثل ما إذا كانت المعادلة معروضة ضمن النص أو معروضة على سطر خاص بها.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## ملاحظات

لا ينطبق نوع تنسيق العرض إلا على المستوى الأعلى من Office Math.

نوع تنسيق العرض الذي تم إرجاعه هو دائمًاInline للرياضيات المكتبية المتداخلة.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../../aspose.words.math/)
* المجسم [Aspose.Words](../../../)
