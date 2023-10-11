---
title: Enum OfficeMathDisplayType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Math.OfficeMathDisplayType تعداد. يحدد نوع تنسيق عرض المعادلة.
type: docs
weight: 4130
url: /ar/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

يحدد نوع تنسيق عرض المعادلة.

```csharp
public enum OfficeMathDisplayType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Display | `0` | يتم عرض Office Math في السطر الخاص بها. |
| Inline | `1` | يتم عرض Office Math سطريًا مع النص. |

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

* مساحة الاسم [Aspose.Words.Math](../../aspose.words.math/)
* المجسم [Aspose.Words](../../)


