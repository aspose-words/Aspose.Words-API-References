---
title: PdfSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words for .NET
description: PdfSaveOptions UseBookFoldPrintingSettings mülk. Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir boole değeri alır veya ayarlar ile belirtilirseMultiplePages  C#'da.
type: docs
weight: 300
url: /tr/net/aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/
---
## PdfSaveOptions.UseBookFoldPrintingSettings property

Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir boole değeri alır veya ayarlar, ile belirtilirse[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Notlar

Bu seçenek belirtilirse,[`PageSet`](../../fixedpagesaveoptions/pageset/) kaydederken göz ardı edilir. Bu davranış MS Word ile eşleşir. Kitap katlama yazdırma ayarları sayfa düzeninde belirtilmezse bu seçeneğin hiçbir etkisi olmayacaktır.

## Örnekler

Bir belgenin PDF formatında kitap katlama biçiminde nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// İçeriği düzenlemek için "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın
// çıktı PDF'sini kitapçık oluşturmak için kullanmamıza yardımcı olacak şekilde.
// PDF'yi normal şekilde oluşturmak için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
options.UseBookFoldPrintingSettings = renderTextAsBookfold;

// Eğer belgeyi kitapçık olarak işliyorsak "Birden Çok Sayfa" ayarını yapmalıyız
// tüm bölümlerin sayfa kurulum nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak ayarlayın.
if (renderTextAsBookfold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Bu belgeyi sayfaların her iki tarafına da yazdırdıktan sonra tüm sayfaları aynı anda ortadan katlayabiliriz,
// ve içerikler kitapçık oluşturacak şekilde sıralanacaktır.
doc.Save(ArtifactsDir + "PdfSaveOptions.SaveAsPdfBookFold.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
