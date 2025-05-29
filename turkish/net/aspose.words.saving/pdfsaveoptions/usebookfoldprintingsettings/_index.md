---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: .NET için Aspose.Words
description: Gelişmiş yazdırma verimliliği için belgeleri kitapçık düzeninde kolayca kaydetmek üzere PdfSaveOptions UseBookFoldPrintingSettings özelliğini keşfedin.
type: docs
weight: 320
url: /tr/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir Boole değeri alır veya ayarlar, bu şekilde belirtilmişse[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Notlar

Bu seçenek belirtilirse,[`PageSet`](../../fixedpagesaveoptions/pageset/) kaydedilirken göz ardı edilir. Bu davranış MS Word ile eşleşir. Kitap katlama yazdırma ayarları sayfa düzeninde belirtilmemişse, bu seçeneğin hiçbir etkisi olmaz.

## Örnekler

Bir belgenin kitap katlaması şeklinde PDF formatına nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// İçeriği düzenlemek için "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın
// çıktı PDF'inde kitapçık yapmak için kullanmamıza yardımcı olacak bir şekilde.
// PDF'yi normal şekilde işlemek için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Belgeyi kitapçık olarak oluşturuyorsak, "Çoklu Sayfalar"ı ayarlamalıyız
// tüm bölümlerin sayfa kurulumu nesnelerinin özellikleri "MultiplePagesType.BookFoldPrinting" olarak değiştirildi.
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Bu belgeyi sayfaların her iki tarafına da yazdırdığımızda, tüm sayfaları aynı anda ortadan katlayabiliriz,
// ve içerikler bir kitapçık oluşturacak şekilde sıralanacaktır.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
