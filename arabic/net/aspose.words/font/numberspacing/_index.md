---
title: Font.NumberSpacing
linktitle: NumberSpacing
articleTitle: NumberSpacing
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font NumberSpacing لتخصيص المسافات بين الأرقام لتحسين سهولة القراءة والتصميم. حسّن أسلوب طباعتك اليوم!
type: docs
weight: 290
url: /ar/net/aspose.words/font/numberspacing/
---
## Font.NumberSpacing property

يحصل على نوع المسافة للرقم الذي يتم عرضه أو يعينه.

```csharp
public NumSpacing NumberSpacing { get; set; }
```

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

* enum [NumSpacing](../../numspacing/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
