---
title: AsposeWordsPrintDocument.CachePrinterSettings
linktitle: CachePrinterSettings
articleTitle: CachePrinterSettings
second_title: .NET için Aspose.Words
description: Yazdırma gecikmelerini en aza indirmek ve performansı artırmak için PrinterSettings'i optimize eden Aspose.Words'ün CachePrinterSettings yöntemiyle yazdırma verimliliğini artırın.
type: docs
weight: 40
url: /tr/net/aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/
---
## AsposeWordsPrintDocument.CachePrinterSettings method

Bazı alanları okur ve önbelleğe alırPrinterSettings baskı süresini azaltmak için.

```csharp
public void CachePrinterSettings()
```

## Notlar

Bu yöntem, daha önce yürütülmemişse yazdırma başlamadan önce çağrılır.

## Örnekler

Belgenin yazdırılacağı sayfa aralığının ve yazıcının nasıl seçileceğini ve ardından baskı önizlemesinin nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Baskı önizleme formunun en üstte gösterilmesi için "Show" metodunu çağırın.
previewDlg.Show();

// Yazdırma İletişim Kutusunu belgedeki sayfa sayısıyla başlat.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// .NET yazdırma belgesinin "Aspose.Words" uygulamasını oluşturun,
// ve ardından yazıcı ayarlarını iletişim kutusundan geçirin.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Yeni renkli yazdırma modunu belirtin.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// "Print" metodunun ilk çağrısının süresini azaltmak için "CachePrinterSettings" metodunu kullanın.
awPrintDoc.CachePrinterSettings();

// Baskı önizlemesinin en üstte gösterilmesi için "Gizle" ve ardından "Önizlemeyi Geçersiz Kıl" yöntemlerini çağırın.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// "Aspose.Words" yazdırma belgesini .NET Baskı Önizleme iletişim kutusuna geçirin.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Ayrıca bakınız

* class [AsposeWordsPrintDocument](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
