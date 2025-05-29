---
title: BaselineAlignment Enum
linktitle: BaselineAlignment
articleTitle: BaselineAlignment
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.BaselineAlignment لتحديد موضع الخط بدقة. حسّن تنسيق مستندك مع خيارات محاذاة رأسية مثالية.
type: docs
weight: 130
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
| Top | `0` | محاذاة على طول الجزء العلوي من كل خط. |
| Center | `1` | يقوم بمحاذاة النقاط المركزية لكل خط. |
| Baseline | `2` | يتماشى مع خط الأساس للفقرة. |
| Bottom | `3` | محاذاة أسفل كل خط. |
| Auto | `4` | يتم تعديل خط الأساس تلقائيًا. |

## أمثلة

يوضح كيفية تعيين الموضع الرأسي للخطوط على خط ما.

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
