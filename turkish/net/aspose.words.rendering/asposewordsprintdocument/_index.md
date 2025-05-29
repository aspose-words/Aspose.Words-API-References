---
title: AsposeWordsPrintDocument Class
linktitle: AsposeWordsPrintDocument
articleTitle: AsposeWordsPrintDocument
second_title: .NET için Aspose.Words
description: Aspose.Words.Rendering ile belge yazdırmayı kolaylaştırın. AsposeWordsPrintDocument sınıfımız .NET uygulamaları için kusursuz entegrasyon sunar.
type: docs
weight: 5260
url: /tr/net/aspose.words.rendering/asposewordsprintdocument/
---
## AsposeWordsPrintDocument class

Bir yazdırma için varsayılan bir uygulama sağlar[`Document`](../../aspose.words/document/)within .NET yazdırma çerçevesi.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Programlama Yoluyla veya İletişim Kutularını Kullanarak Yazdırma](https://docs.aspose.com/words/net/print-a-document-programmatically-or-using-dialogs/) belgeleme makalesi.

```csharp
public class AsposeWordsPrintDocument : PrintDocument
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [AsposeWordsPrintDocument](asposewordsprintdocument/)(*[Document](../../aspose.words/document/)*) | Bu sınıfın yeni bir örneğini başlatır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ColorMode](../../aspose.words.rendering/asposewordsprintdocument/colormode/) { get; set; } | Aygıt renkli yazdırmayı destekliyorsa renkli olmayan sayfaların nasıl yazdırılacağını alır veya ayarlar. |
| [ColorPagesPrinted](../../aspose.words.rendering/asposewordsprintdocument/colorpagesprinted/) { get; } | Renkli olarak yazdırılan sayfa sayısını alır (yaniColor doğru olarak ayarlandı). |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [CachePrinterSettings](../../aspose.words.rendering/asposewordsprintdocument/cacheprintersettings/)() | Bazı alanları okur ve önbelleğe alırPrinterSettings baskı süresini azaltmak için. |

## Notlar

`AsposeWordsPrintDocument` geçersiz kılmalarPrintEventArgs) belirtilen sayfa aralığını yazdırmak içinPrinterSettings.

Tek bir Word belgesi, farklı boyutlarda, yönlendirmelerde ve kağıt tepsilerinde sayfaları belirten birden fazla bölümden oluşabilir.`AsposeWordsPrintDocument` geçersiz kılmalar QueryPageSettingsEventArgs) Word belgesi yazdırırken kağıt boyutunu, orientation ve kağıt kaynağını doğru şekilde seçmek için.

Microsoft Word, bir Word belgesinde kağıt tepsileri için yazıcıya özgü değerleri depolar ve bu nedenle, yalnızca kullanıcı kağıt tepsilerini belirttiğinde seçilen yazıcı modeliyle aynı yazıcı modelinde yazdırmak doğru tepsilerden yazdırmayla sonuçlanacaktır. Belgeyi farklı bir yazıcıda yazdırırsanız, büyük olasılıkla belgede belirtilen tepsiler değil, varsayılan kağıt tepsisi kullanılacaktır.

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
