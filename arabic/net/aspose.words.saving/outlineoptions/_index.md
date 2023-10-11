---
title: Class OutlineOptions
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.OutlineOptions فصل. يسمح بتحديد خيارات المخطط التفصيلي.
type: docs
weight: 5360
url: /ar/net/aspose.words.saving/outlineoptions/
---
## OutlineOptions class

يسمح بتحديد خيارات المخطط التفصيلي.

لمعرفة المزيد، قم بزيارة[حفظ مستند](https://docs.aspose.com/words/net/save-a-document/) مقالة توثيقية.

```csharp
public class OutlineOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [OutlineOptions](outlineoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [BookmarksOutlineLevels](../../aspose.words.saving/outlineoptions/bookmarksoutlinelevels/) { get; } | يسمح بتحديد مستوى المخطط التفصيلي للإشارات المرجعية الفردية. |
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | الحصول على قيمة أو تعيينها لتحديد ما إذا كان سيتم إنشاء مستويات مخطط تفصيلي مفقودة أم لا عندما يتم تصدير المستند . |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | يحدد ما إذا كان سيتم إنشاء مخططات تفصيلية للعناوين (الفقرات المنسقة باستخدام أنماط العناوين) داخل الجداول أم لا. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | يحدد المستوى الافتراضي في المخطط التفصيلي للمستند الذي سيتم عرض إشارات Word المرجعية فيه. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | يحدد عدد المستويات في المخطط التفصيلي للمستند الذي سيتم إظهاره موسعًا عند عرض الملف. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | يحدد عدد مستويات العناوين (الفقرات المنسقة باستخدام أنماط العناوين) التي سيتم تضمينها في مخطط المستند . |

### أمثلة

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


