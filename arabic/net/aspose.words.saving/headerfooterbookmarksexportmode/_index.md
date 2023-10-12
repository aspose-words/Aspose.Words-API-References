---
title: Enum HeaderFooterBookmarksExportMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Saving.HeaderFooterBookmarksExportMode تعداد. يحدد كيفية تصدير الإشارات المرجعية في الرؤوس/التذييلات.
type: docs
weight: 5050
url: /ar/net/aspose.words.saving/headerfooterbookmarksexportmode/
---
## HeaderFooterBookmarksExportMode enumeration

يحدد كيفية تصدير الإشارات المرجعية في الرؤوس/التذييلات.

```csharp
public enum HeaderFooterBookmarksExportMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| None | `0` | لا يتم تصدير الإشارات المرجعية في الرؤوس/التذييلات. |
| First | `1` | يتم تصدير الإشارة المرجعية فقط في الرأس/التذييل الأول للقسم. |
| All | `2` | يتم تصدير الإشارات المرجعية في جميع الرؤوس/التذييلات. |

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


