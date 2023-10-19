---
title: ColorPrintMode Enum
linktitle: ColorPrintMode
articleTitle: ColorPrintMode
second_title: Aspose.Words for .NET
description: Aspose.Words.Rendering.ColorPrintMode Sıralama. Aygıtın renkli yazdırmayı desteklemesi durumunda renkli olmayan sayfaların nasıl yazdırılacağını belirtir C#'da.
type: docs
weight: 4540
url: /tr/net/aspose.words.rendering/colorprintmode/
---
## ColorPrintMode enumeration

Aygıtın renkli yazdırmayı desteklemesi durumunda, renkli olmayan sayfaların nasıl yazdırılacağını belirtir.

```csharp
public enum ColorPrintMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Normal | `0` | Tüm sayfalar yazıcının yeteneklerine ve ayarlarına göre yazdırılır. |
| GrayscaleAuto | `1` | Renkli olmayan sayfalar tespit edilirse gri tonlamalı olarak yazdırılır. |

## Örnekler

Belgenin yazdırılacağı sayfa aralığının ve yazıcının nasıl seçileceğini ve ardından bir baskı önizlemesinin nasıl açılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Baskı önizleme formunun üstte görünmesini sağlamak için "Göster" yöntemini çağırın.
previewDlg.Show();

// Belgedeki sayfa sayısıyla Yazdırma İletişim Kutusunu başlatın.
PrintDialog printDlg = new PrintDialog();
printDlg.AllowSomePages = true;
printDlg.PrinterSettings.MinimumPage = 1;
printDlg.PrinterSettings.MaximumPage = doc.PageCount;
printDlg.PrinterSettings.FromPage = 1;
printDlg.PrinterSettings.ToPage = doc.PageCount;

if (printDlg.ShowDialog() != DialogResult.OK)
    return;

// .NET yazdırma belgesinin "Aspose.Words" uygulamasını oluşturun,
// ve ardından iletişim kutusundan yazıcı ayarlarını aktarın.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// Yeni renkli yazdırma modunu belirtin.
awPrintDoc.ColorMode = ColorPrintMode.GrayscaleAuto;

// "Print" yönteminin ilk çağrılma süresini azaltmak için "CachePrinterSettings" yöntemini kullanın.
awPrintDoc.CachePrinterSettings();

// Baskı önizlemesinin en üstte görünmesini sağlamak için "Gizle"yi ve ardından "GeçersizÖn İzleme" yöntemlerini çağırın.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// "Aspose.Words" yazdırma belgesini .NET Baskı Önizleme iletişim kutusuna aktarın.
previewDlg.Document = awPrintDoc;
previewDlg.ShowDialog();

awPrintDoc.Print();            
Console.WriteLine($"The numer of pages printed in color are {awPrintDoc.ColorPagesPrinted}.");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Rendering](../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../)
