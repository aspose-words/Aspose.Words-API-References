---
title: XpsSaveOptions.UseBookFoldPrintingSettings
second_title: Aspose.Words for .NET API Referansı
description: XpsSaveOptions mülk. Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir boole değeri alır veya ayarlar ile belirtilirseMultiplePages .
type: docs
weight: 40
url: /tr/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir boole değeri alır veya ayarlar, ile belirtilirse[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

### Notlar

Bu seçenek belirtilirse,[`PageSet`](../../fixedpagesaveoptions/pageset/) kaydederken göz ardı edilir. Bu davranış MS Word ile eşleşir. Kitap katlama yazdırma ayarları sayfa düzeninde belirtilmezse bu seçeneğin hiçbir etkisi olmayacaktır.

### Örnekler

Bir belgenin XPS formatında kitap katlama biçiminde nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e dönüştürme biçimini değiştirmek için.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// İçeriği düzenlemek için "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın
// XPS çıktısını kitapçık yapmak için kullanmamıza yardımcı olacak şekilde.
// XPS'yi normal şekilde oluşturmak için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Eğer belgeyi kitapçık olarak işliyorsak "Birden Çok Sayfa" ayarını yapmalıyız
// tüm bölümlerin sayfa kurulum nesnelerinin özelliklerini "MultiplePagesType.BookFoldPrinting" olarak ayarlayın.
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Bu belgeyi yazdırdıktan sonra sayfaları istifleyerek kitapçığa dönüştürebiliriz
// yazıcıdan çıkıp ortadan katlamak için.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Ayrıca bakınız

* class [XpsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../xpssaveoptions/)
* toplantı [Aspose.Words](../../../)


