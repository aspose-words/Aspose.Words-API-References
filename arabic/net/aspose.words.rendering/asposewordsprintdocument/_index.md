---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: Aspose.Words لـ .NET
description: سهّل طباعة المستندات باستخدام Aspose.Words.Rendering. توفر فئة AsposeWordsPrintDocument تكاملاً سلسًا مع تطبيقات .NET.
type: docs
weight: 5260
url: /ar/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

يوفر تنفيذًا افتراضيًا لطباعة[`Document`](../../aspose.words/document/)within إطار عمل الطباعة .NET.

لمعرفة المزيد، قم بزيارة[طباعة مستند برمجيًا أو باستخدام مربعات الحوار](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) مقالة توثيقية.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | يقوم بتهيئة مثيل جديد لهذه الفئة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | يحصل على كيفية طباعة الصفحات غير الملونة أو يعينها إذا كان الجهاز يدعم الطباعة الملونة. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | يحصل على عدد الصفحات المطبوعة بالألوان (أي معColor تم ضبطه على true). |

## طُرق

| اسم | وصف |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | يقرأ ويخزن بعض الحقول في ذاكرة التخزين المؤقتPrinterSettings لتقليل وقت الطباعة. |

## ملاحظات

`AsposeWordsPrintDocument` تجاوزاتPrintEventArgs) لطباعة نطاق الصفحات المحددة فيPrinterSettings.

يمكن أن يتكون مستند Word واحد من أقسام متعددة تحدد صفحات ذات أحجام واتجاهات وأدراج ورق مختلفة.`AsposeWordsPrintDocument` تجاوزات QueryPageSettingsEventArgs) لتحديد حجم الورق والاتجاه ومصدر الورق بشكل صحيح عند طباعة مستند Word.

يخزّن مايكروسوفت وورد قيمًا خاصة بالطابعة لأدراج الورق في مستند وورد، وبالتالي، فإن الطباعة باستخدام نفس طراز الطابعة التي حددها المستخدم عند تحديد أدراج الورق، سيؤدي إلى الطباعة من الأدراج الصحيحة. إذا طبعت مستندًا على طابعة مختلفة، فمن المرجح استخدام درج الورق الافتراضي، وليس الأدراج المحددة في المستند.

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

* مساحة الاسم [Aspose.Words.Rendering](../../aspose.words.rendering/)
* المجسم [Aspose.Words](../../)
