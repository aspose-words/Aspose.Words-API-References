---
title: Enum PdfPageMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.PdfPageMode تعداد. يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF.
type: docs
weight: 5500
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
| UseNone | `0` | لا يمكن رؤية المخطط التفصيلي للمستند أو الصور المصغرة. |
| UseOutlines | `1` | المخطط التفصيلي للمستند مرئي. لاحظ أنه إذا لم يكن هناك مخططات تفصيلية في مستند PDF، فلن يكون جزء التنقل في المخطط التفصيلي مرئيًا على أي حال. |
| UseThumbs | `2` | الصور المصغرة مرئية. |
| FullScreen | `3` | وضع ملء الشاشة، مع عدم وجود شريط قوائم أو عناصر تحكم في النافذة أو أي نافذة أخرى مرئية. |
| UseOC | `4` | لوحة مجموعة المحتوى الاختيارية مرئية. |
| UseAttachments | `5` | لوحة المرفقات مرئية. |

### أمثلة

يوضح كيفية تعيين الإرشادات التي يجب على بعض برامج قراءة PDF اتباعها عند فتح مستند الإخراج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "PageMode" على "PdfPageMode.FullScreen" ليتمكن قارئ PDF من فتح الملفات المحفوظة
// مستند في وضع ملء الشاشة، والذي يسيطر على شاشة العرض ولا يحتوي على عناصر تحكم مرئية.
// اضبط خاصية "PageMode" على "PdfPageMode.UseThumbs" لجعل قارئ PDF يعرض لوحة منفصلة
// مع صورة مصغرة لكل صفحة في المستند.
// قم بتعيين خاصية "PageMode" على "PdfPageMode.UseOC" لجعل قارئ PDF يعرض لوحة منفصلة
// الذي يسمح لنا بالعمل مع أي طبقات موجودة في الوثيقة.
// اضبط خاصية "PageMode" على "PdfPageMode.UseOutlines" للحصول على قارئ PDF
// أيضًا لعرض المخطط التفصيلي، إن أمكن.
// اضبط خاصية "PageMode" على "PdfPageMode.UseNone" لجعل قارئ PDF يعرض المستند نفسه فقط.
// اضبط خاصية "PageMode" على "PdfPageMode.UseAttachments" لجعل لوحة المرفقات مرئية.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

يظهر لمعالجة الإشارات المرجعية في الرؤوس/التذييلات في المستند الذي نعرضه إلى PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// قم بتعيين خاصية "PageMode" على "PdfPageMode.UseOutlines" لعرض جزء التنقل التفصيلي في ملف PDF الناتج.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// قم بتعيين خاصية "DefaultBookmarksOutlineLevel" على "1" لعرض الكل
// الإشارات المرجعية في المستوى الأول من المخطط التفصيلي في ملف PDF الناتج.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// قم بتعيين خاصية "HeaderFooterBookmarksExportMode" على "HeaderFooterBookmarksExportMode.None" إلى
// عدم تصدير أي إشارات مرجعية موجودة داخل الرؤوس/التذييلات.
// قم بتعيين خاصية "HeaderFooterBookmarksExportMode" على "HeaderFooterBookmarksExportMode.First" إلى
// تصدير الإشارات المرجعية فقط في رأس/تذييلات القسم الأول.
// قم بتعيين خاصية "HeaderFooterBookmarksExportMode" على "HeaderFooterBookmarksExportMode.All" إلى
// تصدير الإشارات المرجعية الموجودة في جميع الرؤوس والتذييلات.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


