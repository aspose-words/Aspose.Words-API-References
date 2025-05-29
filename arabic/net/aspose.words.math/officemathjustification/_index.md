---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.Math.OfficeMathJustification enum لمحاذاة المعادلات بدقة. حسّن وضوح مستندك مع خيارات المحاذاة المثالية.
type: docs
weight: 4830
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
| CenterGroup | `1` | يحدد أماكن مثيلات النص الرياضي إلى اليسار بالنسبة لبعضها البعض، ويركز مجموعة النص الرياضي (فقرة الرياضيات) بالنسبة للصفحة. |
| Center | `2` | يقوم بمركز كل مثيل للنص الرياضي بشكل فردي فيما يتعلق بالهوامش. |
| Left | `3` | محاذاة إلى اليسار للفقرة الرياضية. |
| Right | `4` | تبرير صحيح للفقرة الرياضية. |
| Inline | `7` | الموضع المضمن لـ Math. |
| Default | `1` | القيمة الافتراضيةCenterGroup . |

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

* مساحة الاسم [Aspose.Words.Math](../../aspose.words.math/)
* المجسم [Aspose.Words](../../)
