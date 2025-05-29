---
title: HeaderFooterBookmarksExportMode Enum
linktitle: HeaderFooterBookmarksExportMode
articleTitle: HeaderFooterBookmarksExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words.Saving.HeaderFooterBookmarksExportMode على تعزيز تصدير الإشارات المرجعية في الرؤوس والتذييلات لإدارة المستندات بسلاسة.
type: docs
weight: 5800
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
| None | `0` | لا يتم تصدير الإشارات المرجعية الموجودة في الرؤوس/التذييلات. |
| First | `1` | يتم تصدير الإشارة المرجعية فقط في أول رأس/تذييل للقسم. |
| All | `2` | يتم تصدير الإشارات المرجعية في جميع الرؤوس/التذييلات. |

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
