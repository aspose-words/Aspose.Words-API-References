---
title: AsposeWordsPrintDocument
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: .NET için Aspose.Words
description: Uygulamalarınızda belge yazdırmayı kolayca oluşturmak ve yönetmek için Aspose.Words PrintDocument oluşturucusunu keşfedin. Sorunsuz entegrasyonla üretkenliği artırın!
type: docs
weight: 10
url: /tr/net/aspose.words.rendering/asposewordsprintdocument/asposewordsprintdocument/
---
## AsposeWordsPrintDocument constructor

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public AsposeWordsPrintDocument(Document document)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| document | Document | Yazdırılacak belge. |

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

* class [Document](../../../aspose.words/document/)
* class [AsposeWordsPrintDocument](../)
* ad alanı [Aspose.Words.Rendering](../../../aspose.words.rendering/)
* toplantı [Aspose.Words](../../../)
