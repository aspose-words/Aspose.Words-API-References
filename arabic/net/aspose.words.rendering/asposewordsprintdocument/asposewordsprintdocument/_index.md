---
title: AsposeWordsPrintDocument.AsposeWordsPrintDocument
second_title: Aspose.Words لمراجع .NET API
description: AsposeWordsPrintDocument البناء. تهيئة مثيل جديد لهذه الفئة.
type: docs
weight: 10
url: /ar/net/aspose.words.rendering/asposewordsprintdocument/asposewordsprintdocument/
---
## AsposeWordsPrintDocument constructor

تهيئة مثيل جديد لهذه الفئة.

```csharp
public AsposeWordsPrintDocument(Document document)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | المستند المطلوب طباعته. |

### أمثلة

يوضح كيفية تحديد نطاق صفحات وطابعة لطباعة المستند باستخدامهما ، ثم إظهار معاينة قبل الطباعة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// اتصل بطريقة "إظهار" لعرض نموذج معاينة الطباعة في الأعلى.
previewDlg.Show();

// تهيئة مربع حوار الطباعة بعدد الصفحات في المستند.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// إنشاء تنفيذ "Aspose.Words" لمستند طباعة .NET ،
// ثم قم بتمرير إعدادات الطابعة من مربع الحوار.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// استخدم طريقة "CachePrinterSettings" لتقليل وقت المكالمة الأولى لطريقة "الطباعة".
awPrintDoc.CachePrinterSettings();

// قم باستدعاء "إخفاء" ، ثم "InvalidatePreview" للحصول على معاينة قبل الطباعة لتظهر في الأعلى.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// قم بتمرير مستند الطباعة "Aspose.Words" إلى مربع حوار .NET Print Preview.
previewDlg.Document = awPrintDoc;

previewDlg.ShowDialog();
```

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [AsposeWordsPrintDocument](../)
* مساحة الاسم [Aspose.Words.Rendering](../../asposewordsprintdocument/)
* المجسم [Aspose.Words](../../../)


