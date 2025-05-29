---
title: PsSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Belgenizin kaydetme biçimini kolayca belirtmek için PsSaveOptions SaveFormat özelliğini keşfedin. Esnek kaydetme seçenekleriyle iş akışınızı optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
