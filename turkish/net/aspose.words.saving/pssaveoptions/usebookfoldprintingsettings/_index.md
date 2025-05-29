---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: .NET için Aspose.Words
description: Gelişmiş yazdırma verimliliği için belgeleri kitapçık düzeninde kolayca kaydetmek üzere PsSaveOptions UseBookFoldPrintingSettings özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir Boole değeri alır veya ayarlar, bu şekilde belirtilmişse[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Notlar

Bu seçenek belirtilirse,[`PageSet`](../../fixedpagesaveoptions/pageset/) kaydedilirken göz ardı edilir. Bu davranış MS Word ile eşleşir. Kitap katlama yazdırma ayarları sayfa düzeninde belirtilmemişse, bu seçeneğin hiçbir etkisi olmaz.

## Örnekler

Bir belgenin kitap katlaması şeklinde Postscript formatına nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi PostScript'e nasıl dönüştüreceğini değiştirmek için.
// İçeriği düzenlemek için "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın
// çıktı Postscript belgesinde kitapçık yapmamıza yardımcı olacak şekilde.
// Belgeyi normal şekilde kaydetmek için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Belgeyi kitapçık olarak oluşturuyorsak, "Çoklu Sayfalar"ı ayarlamalıyız
// tüm bölümlerin sayfa kurulumu nesnelerinin özellikleri "MultiplePagesType.BookFoldPrinting" olarak değiştirildi.
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Bu belgeyi sayfaların her iki tarafına da yazdırdığımızda, tüm sayfaları aynı anda ortadan katlayabiliriz,
// ve içerikler bir kitapçık oluşturacak şekilde sıralanacaktır.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Ayrıca bakınız

* class [PsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
