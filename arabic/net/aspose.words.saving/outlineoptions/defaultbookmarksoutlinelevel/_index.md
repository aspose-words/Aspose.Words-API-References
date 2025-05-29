---
title: OutlineOptions.DefaultBookmarksOutlineLevel
linktitle: DefaultBookmarksOutlineLevel
articleTitle: DefaultBookmarksOutlineLevel
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية DefaultBookmarksOutlineLevel مستندات Word لديك من خلال تحسين ظهور الإشارات المرجعية في المخطط التفصيلي. عزز إنتاجيتك اليوم!
type: docs
weight: 50
url: /ar/net/aspose.words.saving/outlineoptions/defaultbookmarksoutlinelevel/
---
## OutlineOptions.DefaultBookmarksOutlineLevel property

يحدد المستوى الافتراضي في مخطط المستند الذي سيتم عرض إشارات مرجعية Word فيه.

```csharp
public int DefaultBookmarksOutlineLevel { get; set; }
```

## ملاحظات

يمكن تحديد مستوى الإشارات المرجعية الفردية باستخدام[`BookmarksOutlineLevels`](../bookmarksoutlinelevels/) ملكية.

حدد 0 ولن يتم عرض إشارات مرجعية Word في مخطط المستند. حدد 1 وسيتم عرض إشارات مرجعية Word في مخطط المستند على المستوى 1؛ 2 للمستوى 2 وهكذا.

الإعداد الافتراضي هو 0. النطاق الصالح هو من 0 إلى 9.

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

* class [OutlineOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
