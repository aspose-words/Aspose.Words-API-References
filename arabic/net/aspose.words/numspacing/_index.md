---
title: NumSpacing Enum
linktitle: NumSpacing
articleTitle: NumSpacing
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.NumSpacing enum لتخصيص المسافات بين الأرقام لتحسين تنسيق المستندات. ارتقِ بعرضك النصي اليوم!
type: docs
weight: 5030
url: /ar/net/aspose.words/numspacing/
---
## NumSpacing enumeration

يحدد القيم المحتملة التي يمكن عرض المسافة بين الأرقام فيها.

```csharp
public enum NumSpacing
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Default | `0` | يحدد أن الأرقام يتم عرضها في نموذج الخط الافتراضي. |
| Proportional | `1` | يحدد أن أشكال الأرقام المصممة على أنها متباعدة بشكل متناسب يتم عرضها إذا كان الخط يدعمها. |
| Tabular | `2` | يحدد أن أشكال الأرقام المصممة كجدول يتم عرضها إذا كان الخط يدعمها. |

## أمثلة

يوضح كيفية تعيين نوع المسافة بين الأرقام.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// هذا التأثير مدعوم فقط في الإصدارات الأحدث من MS Word.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2019);

builder.Write("1 ");
builder.Write("This is an example");

Run run = doc.FirstSection.Body.FirstParagraph.Runs[0];
if (run.Font.NumberSpacing == NumSpacing.Default)
    run.Font.NumberSpacing = NumSpacing.Proportional;

doc.Save(ArtifactsDir + "Fonts.NumberSpacing.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
