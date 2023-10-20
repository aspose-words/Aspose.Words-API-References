---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words لـ .NET
description: LayoutOptions ShowParagraphMarks ملكية. الحصول على أو تعيين الإشارة إلى ما إذا كان سيتم عرض علامات الفقرة أم لا. الإعداد الافتراضي هوخطأ شنيع  في C#.
type: docs
weight: 90
url: /ar/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

الحصول على أو تعيين الإشارة إلى ما إذا كان سيتم عرض علامات الفقرة أم لا. الإعداد الافتراضي هو`خطأ شنيع` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## أمثلة

يوضح كيفية إظهار علامات الفقرة في مستند الإخراج المعروض.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// أضف بعض الفقرات، ثم قم بتمكين علامات الفقرات لإظهار نهايات الفقرات
// مع رمز pilcrow (¶) عندما نقوم بعرض المستند.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

### أنظر أيضا

* class [LayoutOptions](../)
* مساحة الاسم [Aspose.Words.Layout](../../../aspose.words.layout/)
* المجسم [Aspose.Words](../../../)
