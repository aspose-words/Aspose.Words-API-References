---
title: AsposeWordsPrintDocument.CachePrinterSettings
linktitle: CachePrinterSettings
articleTitle: CachePrinterSettings
second_title: Aspose.Words لـ .NET
description: قم بتعزيز كفاءة الطباعة باستخدام طريقة CachePrinterSettings في Aspose.Words، والتي تعمل على تحسين PrinterSettings لتقليل تأخيرات الطباعة وتحسين الأداء.
type: docs
weight: 40
url: /ar/net/aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/
---
## AsposeWordsPrintDocument.CachePrinterSettings method

يقرأ ويخزن بعض الحقول في ذاكرة التخزين المؤقتPrinterSettings لتقليل وقت الطباعة.

```csharp
public void CachePrinterSettings()
```

## ملاحظات

يتم استدعاء هذه الطريقة قبل بدء الطباعة إذا لم يتم تنفيذها مسبقًا.

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

* class [AsposeWordsPrintDocument](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
