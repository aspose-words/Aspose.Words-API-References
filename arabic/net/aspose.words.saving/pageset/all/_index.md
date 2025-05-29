---
title: PageSet.All
linktitle: All
articleTitle: All
second_title: Aspose.Words لـ .NET
description: الوصول إلى جميع صفحات المستندات بترتيبها الأصلي باستخدام خاصية "مجموعة الصفحات". بسّط سير عملك وحسّن إدارة مستنداتك بسهولة!
type: docs
weight: 20
url: /ar/net/aspose.words.saving/pageset/all/
---
## PageSet.All property

يحصل على مجموعة تحتوي على جميع صفحات المستند بالترتيب الأصلي.

```csharp
public static PageSet All { get; }
```

## أمثلة

يوضح كيفية تصدير الصفحات الفردية من المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 5; i++)
{
    builder.Writeln($"Page {i + 1} ({(i % 2 == 0 ? "odd" : "even")})");
    if (i < 4)
        builder.InsertBreak(BreakType.PageBreak);
}

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// فيما يلي ثلاث خصائص لـPageSet يمكننا استخدامها لتصفية مجموعة من الصفحات من
// مستندنا لحفظه في مستند PDF ناتج بناءً على تكافؤ أرقام صفحاته.
// 1 - احفظ الصفحات ذات الأرقام الزوجية فقط:
options.PageSet = PageSet.Even;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

// 2 - احفظ الصفحات ذات الأرقام الفردية فقط:
options.PageSet = PageSet.Odd;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

// 3 - احفظ كل صفحة:
options.PageSet = PageSet.All;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportPageSet.All.pdf", options);
```

### أنظر أيضا

* class [PageSet](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
