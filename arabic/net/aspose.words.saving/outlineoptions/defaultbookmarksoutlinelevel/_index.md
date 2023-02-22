---
title: OutlineOptions.DefaultBookmarksOutlineLevel
second_title: Aspose.Words لمراجع .NET API
description: OutlineOptions ملكية. يحدد المستوى الافتراضي في مخطط المستند الذي يتم عنده عرض إشارات مرجعية لـ Word.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

يحدد المستوى الافتراضي في مخطط المستند الذي يتم عنده عرض إشارات مرجعية لـ Word.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

### ملاحظات

يمكن تحديد مستوى الإشارات المرجعية الفردية باستخدام[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) منشأه.

حدد 0 ولن يتم عرض إشارات مرجعية لـ Word في مخطط المستند . حدد 1 وسيتم عرض إشارات مرجعية لـ Word في مخطط المستند في المستوى 1 ؛ 2 للمستوى 2 وما إلى ذلك.

الافتراضي هو 0. النطاق الصالح هو 0 إلى 9.

### أمثلة

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

* class [OutlineOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../outlineoptions/)
* المجسم [Aspose.Words](../../../)


