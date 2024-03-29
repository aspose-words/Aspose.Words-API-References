---
title: OfficeMath.EquationXmlEncoding
second_title: Aspose.Words لمراجع .NET API
description: OfficeMath ملكية. الحصول على / تعيين الترميز الذي تم استخدامه لتشفير معادلة XML  إذا تمت قراءة كائن الرياضيات في المكتب من معادلة XML. نستخدم الترميز عند حفظ مستند لكتابة نفس الترميز الذي تمت قراءته.
type: docs
weight: 20
url: /ar/net/aspose.words.math/officemath/equationxmlencoding/
---
## OfficeMath.EquationXmlEncoding property

الحصول على / تعيين الترميز الذي تم استخدامه لتشفير معادلة XML ، إذا تمت قراءة كائن الرياضيات في المكتب من معادلة XML. نستخدم الترميز عند حفظ مستند لكتابة نفس الترميز الذي تمت قراءته.

```csharp
public Encoding EquationXmlEncoding { get; set; }
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

* class [OfficeMath](../)
* مساحة الاسم [Aspose.Words.Math](../../officemath/)
* المجسم [Aspose.Words](../../../)


