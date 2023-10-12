---
title: PdfSaveOptions.HeaderFooterBookmarksExportMode
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. يحدد كيفية تصدير الإشارات المرجعية في الرؤوس/التذييلات.
type: docs
weight: 180
url: /ar/net/aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/
---
## PdfSaveOptions.HeaderFooterBookmarksExportMode property

يحدد كيفية تصدير الإشارات المرجعية في الرؤوس/التذييلات.

```csharp
public HeaderFooterBookmarksExportMode HeaderFooterBookmarksExportMode { get; set; }
```

### ملاحظات

القيمة الافتراضية هيAll.

يتم استخدام هذه الخاصية بالتزامن مع[`OutlineOptions`](../outlineoptions/) خيار.

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

* enum [HeaderFooterBookmarksExportMode](../../headerfooterbookmarksexportmode/)
* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


