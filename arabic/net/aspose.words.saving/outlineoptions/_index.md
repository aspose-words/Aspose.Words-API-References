---
title: OutlineOptions Class
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.OutlineOptions لتخصيص إعدادات مخطط مستندك لتحسين التنظيم والوضوح.
type: docs
weight: 6140
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
| [BookmarksOutlineLevels](../../aspose.words.saving/outlineoptions/bookmarksoutlinelevels/) { get; } | يسمح بتحديد مستوى الخطوط العريضة للإشارات المرجعية الفردية. |
| [CreateMissingOutlineLevels](../../aspose.words.saving/outlineoptions/createmissingoutlinelevels/) { get; set; } | يحصل على قيمة أو يعينها لتحديد ما إذا كان سيتم إنشاء مستويات مخطط مفقودة أم لا عند تصدير المستند . |
| [CreateOutlinesForHeadingsInTables](../../aspose.words.saving/outlineoptions/createoutlinesforheadingsintables/) { get; set; } | يحدد ما إذا كان سيتم إنشاء مخططات للعناوين (الفقرات المنسقة باستخدام أنماط العناوين) داخل الجداول أم لا. |
| [DefaultBookmarksOutlineLevel](../../aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/) { get; set; } | يحدد المستوى الافتراضي في مخطط المستند الذي سيتم عرض إشارات مرجعية Word فيه. |
| [ExpandedOutlineLevels](../../aspose.words.saving/outlineoptions/expandedoutlinelevels/) { get; set; } | يحدد عدد المستويات في مخطط المستند التي سيتم عرضها موسعة عند عرض الملف. |
| [HeadingsOutlineLevels](../../aspose.words.saving/outlineoptions/headingsoutlinelevels/) { get; set; } | يحدد عدد مستويات العناوين (الفقرات المنسقة باستخدام أنماط العناوين) المراد تضمينها في مخطط المستند . |

## أمثلة

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
