---
title: AsposeWordsPrintDocument.AsposeWordsPrintDocument
second_title: Aspose.Words for .NET API Referansı
description: AsposeWordsPrintDocument inşaatçı. Bu sınıfın yeni bir örneğini başlatır.
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

### Örnekler

Belgeyi yazdırmak için bir sayfa aralığı ve yazıcının nasıl seçileceğini ve ardından bir baskı önizlemesinin nasıl getirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PrintPreviewDialog previewDlg = new PrintPreviewDialog();

// Baskı önizleme formunun en üstte gösterilmesini sağlamak için "Show" yöntemini çağırın.
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
// ve ardından iletişim kutusundan yazıcı ayarlarını geçirin.
AsposeWordsPrintDocument awPrintDoc = new AsposeWordsPrintDocument(doc);
awPrintDoc.PrinterSettings = printDlg.PrinterSettings;

// "Yazdır" yönteminin ilk çağrısının süresini azaltmak için "CachePrinterSettings" yöntemini kullanın.
awPrintDoc.CachePrinterSettings();

// Baskı önizlemenin en üstte gösterilmesini sağlamak için "Gizle" ve ardından "InvalidatePreview" yöntemlerini çağırın.
previewDlg.Hide();
previewDlg.PrintPreviewControl.InvalidatePreview();

// "Aspose.Words" yazdırma belgesini .NET Baskı Önizleme iletişim kutusuna iletin.
previewDlg.Document = awPrintDoc;

previewDlg.ShowDialog();
```

### Ayrıca bakınız

* class [Document](../../../aspose.words/document/)
* class [AsposeWordsPrintDocument](../)
* ad alanı [Aspose.Words.Rendering](../../asposewordsprintdocument/)
* toplantı [Aspose.Words](../../../)


