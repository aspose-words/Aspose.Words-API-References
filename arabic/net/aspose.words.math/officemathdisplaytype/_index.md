---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Math.OfficeMathDisplayType لتخصيص تنسيقات عرض المعادلات بسهولة لتحسين وضوح المستند والعرض.
type: docs
weight: 4820
url: /ar/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

يحدد نوع تنسيق العرض للمعادلة.

```csharp
public enum OfficeMathDisplayType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Display | `0` | يتم عرض الرياضيات المكتبية على سطر خاص بها. |
| Inline | `1` | يتم عرض الرياضيات المكتبية مضمنة مع النص. |

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
