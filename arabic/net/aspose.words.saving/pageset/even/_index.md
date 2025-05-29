---
title: PageSet.Even
linktitle: Even
articleTitle: Even
second_title: Aspose.Words لـ .NET
description: استرجع مجموعة من الصفحات الزوجية من مستندك بترتيبها الأصلي باستخدام PageSet Even. بسّط سير عملك وحسّن إدارة مستنداتك!
type: docs
weight: 30
url: /ar/net/aspose.words.saving/pageset/even/
---
## PageSet.Even property

يحصل على مجموعة تحتوي على جميع الصفحات الزوجية للمستند بالترتيب الأصلي.

```csharp
public static PageSet Even { get; }
```

## ملاحظات

تحتوي الصفحات الزوجية على فهرس فردي لأن فهرس الصفحات يعتمد على الصفر.

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
