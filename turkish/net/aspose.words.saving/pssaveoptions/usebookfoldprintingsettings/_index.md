---
title: PsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: Aspose.Words for .NET
description: PsSaveOptions UseBookFoldPrintingSettings mülk. Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir boole değeri alır veya ayarlar ile belirtilirseMultiplePages  C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/
---
## PsSaveOptions.UseBookFoldPrintingSettings property

Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir boole değeri alır veya ayarlar, ile belirtilirse[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Notlar

Bu seçenek belirtilirse,[`PageSet`](../../fixedpagesaveoptions/pageset/) kaydederken göz ardı edilir. Bu davranış MS Word ile eşleşir. Kitap katlama yazdırma ayarları sayfa düzeninde belirtilmezse bu seçeneğin hiçbir etkisi olmayacaktır.

## Örnekler

Bir belgenin Postscript formatında kitap katlama biçiminde nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi PostScript'e dönüştürme biçimini değiştirmek için.
// İçeriği düzenlemek için "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın
// çıktı Postscript belgesinde, bundan bir kitapçık oluşturmamıza yardımcı olacak şekilde.
// Belgeyi normal şekilde kaydetmek için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Eğer belgeyi kitapçık olarak işliyorsak "Birden Çok Sayfa" ayarını yapmalıyız
// tüm bölümlerin sayfa kurulum nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak ayarlayın.
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Bu belgeyi sayfaların her iki tarafına da yazdırdıktan sonra tüm sayfaları aynı anda ortadan katlayabiliriz,
// ve içerikler kitapçık oluşturacak şekilde sıralanacaktır.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Ayrıca bakınız

* class [PsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
