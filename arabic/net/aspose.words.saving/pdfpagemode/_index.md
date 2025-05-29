---
title: PdfPageMode Enum
linktitle: PdfPageMode
articleTitle: PdfPageMode
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.PdfPageMode enum لخيارات عرض PDF قابلة للتخصيص، مما يُحسّن تجربة المستخدم في أي قارئ PDF. حسّن مستنداتك اليوم!
type: docs
weight: 6300
url: /ar/net/aspose.words.saving/pdfpagemode/
---
## PdfPageMode enumeration

يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF.

```csharp
public enum PdfPageMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| UseNone | `0` | لا يمكن رؤية مخطط المستند أو الصور المصغرة. |
| UseOutlines | `1` | مخطط المستند مرئي. لاحظ أنه إذا لم تكن هناك مخططات في مستند PDF، فلن تكون لوحة التنقل الخاصة بالمخطط مرئية على أي حال. |
| UseThumbs | `2` | الصور المصغرة مرئية. |
| FullScreen | `3` | وضع ملء الشاشة، بدون شريط القائمة، أو عناصر التحكم في النافذة، أو أي نافذة أخرى مرئية. |
| UseOC | `4` | لوحة مجموعة المحتوى الاختيارية مرئية. |
| UseAttachments | `5` | لوحة المرفقات مرئية. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
