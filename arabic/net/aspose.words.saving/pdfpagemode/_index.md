---
title: Enum PdfPageMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.PdfPageMode تعداد. يحدد كيفية عرض مستند PDF عند فتحه في قارئ PDF.
type: docs
weight: 5220
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
| UseNone | `0` | لا يظهر مخطط المستند ولا الصور المصغرة. |
| UseOutlines | `1` | مخطط المستند مرئي. لاحظ أنه في حالة عدم وجود مخططات في مستند PDF ، فلن يكون جزء التنقل بالخطوط الخارجية مرئيًا على أي حال. |
| UseThumbs | `2` | الصور المصغرة مرئية . |
| FullScreen | `3` | وضع ملء الشاشة ، مع عدم وجود شريط قوائم أو عناصر تحكم في النافذة أو أي نافذة أخرى مرئية. |
| UseOC | `4` | لوحة مجموعة المحتوى الاختيارية مرئية . |
| UseAttachments | `5` | لوحة المرفقات مرئية . |

### أمثلة

يوضح كيفية تعيين التعليمات التي يجب على بعض برامج قراءة PDF اتباعها عند فتح مستند ناتج.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions options = new PdfSaveOptions();

// اضبط خاصية "PageMode" على "PdfPageMode.FullScreen" لجعل قارئ PDF يفتح الملف المحفوظ
// المستند في وضع ملء الشاشة ، والذي يستحوذ على شاشة العرض ولا يحتوي على عناصر تحكم مرئية.
// اضبط خاصية "PageMode" على "PdfPageMode.UseThumbs" لجعل قارئ PDF يعرض لوحة منفصلة
// مع صورة مصغرة لكل صفحة في المستند.
// اضبط خاصية "PageMode" على "PdfPageMode.UseOC" لجعل قارئ PDF يعرض لوحة منفصلة
// الذي يسمح لنا بالعمل مع أي طبقات موجودة في المستند.
// اضبط خاصية "PageMode" على "PdfPageMode.UseOutlines" للحصول على قارئ PDF
// أيضًا لعرض المخطط التفصيلي ، إن أمكن.
// اضبط خاصية "PageMode" على "PdfPageMode.UseNone" لجعل قارئ PDF يعرض المستند نفسه فقط.
// اضبط خاصية "PageMode" على "PdfPageMode.UseAttachments" لجعل لوحة المرفقات مرئية.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

يظهر لمعالجة الإشارات المرجعية في الرؤوس / التذييلات في مستند نقوم بتقديمه إلى PDF.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// اضبط خاصية "PageMode" على "PdfPageMode.UseOutlines" لعرض جزء التنقل في المخطط التفصيلي في ملف PDF الناتج.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// اضبط خاصية "DefaultBookmarksOutlineLevel" على "1" لعرض الكل
// الإشارات المرجعية في المستوى الأول من المخطط التفصيلي في ملف PDF الناتج.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// تعيين خاصية "HeaderFooterBookmarksExportMode" على "HeaderFooterBookmarksExportMode.None" إلى
// لا تصدر أي إشارات مرجعية موجودة داخل الرؤوس / التذييلات.
// تعيين خاصية "HeaderFooterBookmarksExportMode" على "HeaderFooterBookmarksExportMode.First" إلى
// فقط تصدير الإشارات المرجعية في رأس / تذييلات القسم الأول.
// تعيين خاصية "HeaderFooterBookmarksExportMode" على "HeaderFooterBookmarksExportMode.All" إلى
// تصدير الإشارات المرجعية الموجودة في جميع الرؤوس / التذييلات.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)


