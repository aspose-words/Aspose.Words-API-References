---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Math.OfficeMathJustification تعداد. يحدد مبرر المعادلة في C#.
type: docs
weight: 4140
url: /ar/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

يحدد مبرر المعادلة.

```csharp
public enum OfficeMathJustification
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| CenterGroup | `1` | ضبط مثيلات النص الرياضي على اليسار بالنسبة لبعضها البعض، وتوسيط مجموعة النص الرياضي (فقرة الرياضيات) بالنسبة للصفحة. |
| Center | `2` | يقوم بتوسيط كل مثيل للنص الرياضي بشكل فردي فيما يتعلق بالهوامش. |
| Left | `3` | التبرير الأيسر للفقرة الرياضية. |
| Right | `4` | التبرير الصحيح للفقرة الرياضية. |
| Inline | `7` | الموضع المضمّن للرياضيات. |
| Default | `1` | القيمة الافتراضيةCenterGroup . |

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

* مساحة الاسم [Aspose.Words.Math](../../aspose.words.math/)
* المجسم [Aspose.Words](../../)
