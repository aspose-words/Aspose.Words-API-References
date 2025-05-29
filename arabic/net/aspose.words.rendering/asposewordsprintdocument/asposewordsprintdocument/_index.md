---
title: AsposeWordsPrintDocument
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words لـ .NET
description: اكتشف مُنشئ طباعة المستندات Aspose.Words لإنشاء وإدارة طباعة المستندات بسهولة في تطبيقاتك. عزز إنتاجيتك بتكامل سلس!
type: docs
weight: 10
url: /ar/net/aspose.words.rendering/asposewordsprintdocument/asposewordsprintdocument/
---
## AsposeWordsPrintDocument constructor

يقوم بتهيئة مثيل جديد لهذه الفئة.

```csharp
public AsposeWordsPrintDocument(Document document)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| document | Document | الوثيقة المراد طباعتها. |

## أمثلة

يوضح كيفية تحديد نطاق الصفحات والطابعة لطباعة المستند، ثم إظهار معاينة الطباعة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// قم باستدعاء طريقة "إظهار" لإظهار نموذج معاينة الطباعة في الأعلى.
previewDlg.Show();

// قم بتهيئة مربع حوار الطباعة بعدد الصفحات الموجودة في المستند.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// قم بإنشاء تنفيذ "Aspose.Words" لمستند الطباعة .NET،
// ثم قم بتمرير إعدادات الطابعة من مربع الحوار.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// حدد وضع الطباعة الملونة الجديد.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// استخدم طريقة "CachePrinterSettings" لتقليل وقت الاستدعاء الأول لطريقة "Print".
awPrintDoc.CachePrinterSettings();

// قم باستدعاء طريقتي "إخفاء"، ثم "InvalidatePreview" لجعل معاينة الطباعة تظهر في الأعلى.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// قم بتمرير مستند الطباعة "Aspose.Words" إلى مربع حوار معاينة الطباعة .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### أنظر أيضا

* class [Document](../../../aspose.words/document/)
* class [AsposeWordsPrintDocument](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
