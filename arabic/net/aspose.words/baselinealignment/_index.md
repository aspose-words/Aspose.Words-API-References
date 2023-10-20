---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words لـ .NET
description: Aspose.Words.BaselineAlignment تعداد. يحدد الموضع الرأسي للخطوط على السطر في C#.
type: docs
weight: 20
url: /ar/net/aspose.words/baselinealignment/
---
## BaselineAlignment enumeration

يحدد الموضع الرأسي للخطوط على السطر.

```csharp
public enum BaselineAlignment
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Top | `0` | محاذاة أعلى كل خط. |
| Center | `1` | محاذاة النقاط المركزية لكل خط. |
| Baseline | `2` | محاذاة إلى الخط الأساسي للفقرة. |
| Bottom | `3` | محاذاة إلى أسفل كل خط. |
| Auto | `4` | يتم ضبط خط الأساس تلقائيًا. |

## أمثلة

يوضح كيفية ضبط الوضع الرأسي للخطوط على السطر.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;
if (format.BaselineAlignment == BaselineAlignment.Auto)
{                
    format.BaselineAlignment = BaselineAlignment.Top;
}

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphBaselineAlignment.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
