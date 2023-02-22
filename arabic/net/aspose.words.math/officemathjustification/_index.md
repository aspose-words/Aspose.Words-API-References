---
title: Enum OfficeMathJustification
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Math.OfficeMathJustification تعداد. تحديد مبرر المعادلة .
type: docs
weight: 3900
url: /ar/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

تحديد مبرر المعادلة .

```csharp
public enum OfficeMathJustification
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| CenterGroup | `1` | يبرر مثيلات النص الرياضي إلى اليسار فيما يتعلق ببعضها البعض ، ويضع مجموعة النص الرياضي_ في الوسط (فقرة الرياضيات) فيما يتعلق بالصفحة . |
| Center | `2` | توسيط كل مثيل من النص الرياضي بشكل فردي بالنسبة للهوامش. |
| Left | `3` | التبرير الأيسر للفقرة الحسابية . |
| Right | `4` | التبرير الصحيح للفقرة الرياضيات . |
| Inline | `7` | موضع مضمّن للرياضيات . |
| Default | `1` | القيمة الافتراضيةCenterGroup . |

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

* مساحة الاسم [Aspose.Words.Math](../../aspose.words.math/)
* المجسم [Aspose.Words](../../)


