---
title: FixedPageSaveOptions.PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words لـ .NET
description: تحكم في عرض مستنداتك باستخدام مجموعة صفحات FixedPageSaveOptions. اختر بسهولة صفحات محددة أو اختر جميعها لإخراج سلس. حسّن سير عملك!
type: docs
weight: 70
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/pageset/
---
## FixedPageSaveOptions.PageSet property

يحصل على الصفحات التي سيتم عرضها أو يعينها. الافتراضي هو كل الصفحات الموجودة في المستند.

```csharp
public PageSet PageSet { get; set; }
```

## أمثلة

يوضح كيفية استخراج الصفحات استنادًا إلى مؤشرات الصفحات الدقيقة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//أضف خمس صفحات إلى المستند.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// قم بإنشاء كائن "XpsSaveOptions"، والذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// استخدم خاصية "PageSet" لتحديد مجموعة من صفحات المستند لحفظها في تنسيق XPS الناتج.
// في هذه الحالة سوف نختار، من خلال فهرس يعتمد على الصفر، ثلاث صفحات فقط: الصفحة 1، والصفحة 2، والصفحة 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

يوضح كيفية تحويل بعض الصفحات فقط في مستند إلى PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

using (Stream stream = File.Create(ArtifactsDir + "PdfSaveOptions.OnePage.pdf"))
{
    // قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
    // لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
    PdfSaveOptions options = new PdfSaveOptions();

    // قم بتعيين "PageIndex" إلى "1" لعرض جزء من المستند بدءًا من الصفحة الثانية.
    options.PageSet = new PageSet(1);

    // ستحتوي هذه الوثيقة على صفحة واحدة بدءًا من الصفحة الثانية، والتي ستحتوي فقط على الصفحة الثانية.
    doc.Save(stream, options);
}
```

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

* class [PageSet](../../pageset/)
* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
