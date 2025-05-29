---
title: PdfSaveOptions.HeaderFooterBookmarksExportMode
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية PdfSaveOptions HeaderFooterBookmarksExportMode على تحسين تصدير الإشارات المرجعية في الرؤوس والتذييلات لتحسين وظائف PDF.
type: docs
weight: 180
url: /ar/net/aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/
---
## PdfSaveOptions.HeaderFooterBookmarksExportMode property

يحدد كيفية تصدير الإشارات المرجعية في الرؤوس/التذييلات.

```csharp
public HeaderFooterBookmarksExportMode HeaderFooterBookmarksExportMode { get; set; }
```

## ملاحظات

القيمة الافتراضية هيAll.

يتم استخدام هذه الخاصية بالتزامن مع[`OutlineOptions`](../outlineoptions/) خيار.

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

* enum [HeaderFooterBookmarksExportMode](../../headerfooterbookmarksexportmode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
