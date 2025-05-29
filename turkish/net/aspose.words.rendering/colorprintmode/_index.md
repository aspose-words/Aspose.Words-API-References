---
title: ColorPrintMode Enum
linktitle: ColorPrintMode
articleTitle: ColorPrintMode
second_title: .NET için Aspose.Words
description: Optimize edilmiş renkli baskı için Aspose.Words.Rendering.ColorPrintMode enum'unu keşfedin. Gelişmiş belge kalitesi için renkli olmayan sayfaların nasıl yazdırılacağını kontrol edin.
type: docs
weight: 5270
url: /tr/net/aspose.words.rendering/colorprintmode/
---
## ColorPrintMode enumeration

Aygıt renkli yazdırmayı destekliyorsa renkli olmayan sayfaların nasıl yazdırılacağını belirtir.

```csharp
public enum ColorPrintMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Normal | `0` | Tüm sayfalar yazıcının yeteneklerine ve ayarlarına göre yazdırılır. |
| GrayscaleAuto | `1` | Algılanan renklendirilmemiş sayfalar gri tonlamalı olarak yazdırılır. |

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

* ad alanı [Aspose.Words.Rendering](../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../)
