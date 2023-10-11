---
title: OfficeMath.Justification
second_title: Aspose.Words لمراجع .NET API
description: OfficeMath ملكية. الحصول على/تعيين مبررات Office Math.
type: docs
weight: 20
url: /ar/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

الحصول على/تعيين مبررات Office Math.

```csharp
public OfficeMathJustification Justification { get; set; }
```

### ملاحظات

لا يمكن تعيين التبرير على Office Math مع نوع تنسيق العرضInline.

لا يمكن تعيين الضبط المضمّن على Office Math مع نوع تنسيق العرضDisplay.

مُتَجَانِس[`DisplayType`](../displaytype/) يجب تعيينه قبل تعيين مبرر Office Math.

### أمثلة

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../officemath/)
* المجسم [Aspose.Words](../../../)


