---
title: PdfSaveOptions.PageMode
linktitle: PageMode
articleTitle: PageMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية PageMode في PdfSaveOptions على تعزيز تجربة عرض ملفات PDF من خلال تخصيص عرض المستندات في أي قارئ PDF.
type: docs
weight: 260
url: /ar/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF.

```csharp
public PdfPageMode PageMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيUseOutlines .

## أمثلة

يوضح كيفية تعيين التعليمات التي يجب على بعض قارئي PDF اتباعها عند فتح مستند إخراج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "PageMode" على "PdfPageMode.FullScreen" لجعل قارئ PDF يفتح الملف المحفوظ
// مستند في وضع ملء الشاشة، والذي يتولى عرض الشاشة ولا يحتوي على أي عناصر تحكم مرئية.
// اضبط خاصية "PageMode" على "PdfPageMode.UseThumbs" لجعل قارئ PDF يعرض لوحة منفصلة
// مع صورة مصغرة لكل صفحة في المستند.
// اضبط خاصية "PageMode" على "PdfPageMode.UseOC" لجعل قارئ PDF يعرض لوحة منفصلة
// الذي يسمح لنا بالعمل مع أي طبقات موجودة في المستند.
// اضبط خاصية "PageMode" على "PdfPageMode.UseOutlines" للحصول على قارئ PDF
//أيضًا لعرض المخطط التفصيلي، إذا كان ذلك ممكنًا.
// قم بضبط خاصية "PageMode" على "PdfPageMode.UseNone" لجعل قارئ PDF يعرض المستند نفسه فقط.
// قم بتعيين خاصية "PageMode" إلى "PdfPageMode.UseAttachments" لجعل لوحة المرفقات مرئية.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

يوضح كيفية معالجة الإشارات المرجعية في الرؤوس/التذييلات في المستند الذي نقوم بتحويله إلى PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// قم بتعيين خاصية "PageMode" إلى "PdfPageMode.UseOutlines" لعرض جزء التنقل المخطط التفصيلي في ملف PDF الناتج.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// اضبط خاصية "DefaultBookmarksOutlineLevel" على "1" لعرض جميع
// إشارات مرجعية في المستوى الأول من المخطط التفصيلي في ملف PDF الناتج.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// اضبط خاصية "HeaderFooterBookmarksExportMode" إلى "HeaderFooterBookmarksExportMode.None"
// لا يتم تصدير أي إشارات مرجعية موجودة داخل الرؤوس/التذييلات.
// اضبط خاصية "HeaderFooterBookmarksExportMode" إلى "HeaderFooterBookmarksExportMode.First" إلى
// تصدير الإشارات المرجعية فقط في رأس/تذييل القسم الأول.
// اضبط خاصية "HeaderFooterBookmarksExportMode" إلى "HeaderFooterBookmarksExportMode.All" إلى
// تصدير الإشارات المرجعية الموجودة في كافة الرؤوس والتذييلات.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### أنظر أيضا

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
