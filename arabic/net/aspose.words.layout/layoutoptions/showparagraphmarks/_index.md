---
title: LayoutOptions.ShowParagraphMarks
linktitle: ShowParagraphMarks
articleTitle: ShowParagraphMarks
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية LayoutOptions ShowParagraphMarks تنسيق النص بتبديل ظهور علامات الفقرات. حسّن وضوح مستندك اليوم!
type: docs
weight: 90
url: /ar/net/aspose.words.layout/layoutoptions/showparagraphmarks/
---
## LayoutOptions.ShowParagraphMarks property

يحصل على أو يعين مؤشرًا لما إذا كانت علامات الفقرة يتم عرضها أم لا. الافتراضي هو`خطأ شنيع` .

```csharp
public bool ShowParagraphMarks { get; set; }
```

## أمثلة

يوضح كيفية إظهار علامات الفقرات في مستند الإخراج المقدم.

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
