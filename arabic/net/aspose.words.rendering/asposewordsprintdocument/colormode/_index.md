---
title: AsposeWordsPrintDocument.ColorMode
linktitle: ColorMode
articleTitle: ColorMode
second_title: Aspose.Words لـ .NET
description: AsposeWordsPrintDocument ColorMode ملكية. الحصول على أو تعيين كيفية طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة الملونة في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.rendering/asposewordsprintdocument/colormode/
---
## AsposeWordsPrintDocument.ColorMode property

الحصول على أو تعيين كيفية طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة الملونة.

```csharp
public ColorPrintMode ColorMode { get; set; }
```

## ملاحظات

لا يؤثر على طباعة الكتيبات.

## أمثلة

يوضح كيفية تحديد نطاق صفحات وطابعة لطباعة المستند بها، ثم إظهار معاينة الطباعة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// اتصل بالطريقة "إظهار" للحصول على نموذج معاينة الطباعة ليظهر في الأعلى.
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

// إنشاء تطبيق "Aspose.Words" لمستند الطباعة .NET،
// ثم قم بتمرير إعدادات الطابعة من مربع الحوار.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// حدد وضع الطباعة الملونة الجديد.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// استخدم طريقة "CachePrinterSettings" لتقليل وقت الاستدعاء الأول لطريقة "الطباعة".
awPrintDoc.CachePrinterSettings();

// اتصل بطرق "Hide"، ثم طرق "InvalidatePreview" للحصول على معاينة الطباعة لتظهر في الأعلى.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// قم بتمرير مستند الطباعة "Aspose.Words" إلى مربع حوار معاينة الطباعة في .NET.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();            
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### أنظر أيضا

* enum [ColorPrintMode](../../colorprintmode/)
* class [AsposeWordsPrintDocument](../)
* مساحة الاسم [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../../)
