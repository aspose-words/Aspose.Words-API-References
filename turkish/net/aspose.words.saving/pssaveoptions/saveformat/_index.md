---
title: PsSaveOptions.SaveFormat
second_title: Aspose.Words for .NET API Referansı
description: PsSaveOptions mülk. Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaPs .
type: docs
weight: 20
url: /tr/net/aspose.words.saving/pssaveoptions/saveformat/
---
## PsSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. YalnızcaPs .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Örnekler

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pssaveoptions/)
* toplantı [Aspose.Words](../../../)


