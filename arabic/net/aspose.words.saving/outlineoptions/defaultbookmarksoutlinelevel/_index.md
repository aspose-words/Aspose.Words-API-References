---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words لـ .NET
description: OutlineOptions DefaultBookmarksOutlineLevel ملكية. يحدد المستوى الافتراضي في المخطط التفصيلي للمستند الذي سيتم عرض إشارات Word المرجعية فيه في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

يحدد المستوى الافتراضي في المخطط التفصيلي للمستند الذي سيتم عرض إشارات Word المرجعية فيه.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## ملاحظات

يمكن تحديد مستوى الإشارات المرجعية الفردية باستخدام[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) ملكية.

حدد 0 ولن يتم عرض الإشارات المرجعية لـ Word في المخطط التفصيلي للمستند. حدد 1 وسيتم عرض الإشارات المرجعية لـ Word في المخطط التفصيلي للمستند في المستوى 1؛ 2 للمستوى 2 وهكذا.

الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

## أمثلة

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

* class [OutlineOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
