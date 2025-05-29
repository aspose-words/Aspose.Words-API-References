---
title: XpsSaveOptions.UseBookFoldPrintingSettings
linktitle: UseBookFoldPrintingSettings
articleTitle: UseBookFoldPrintingSettings
second_title: .NET için Aspose.Words
description: XpsSaveOptions UseBookFoldPrintingSettings özelliğiyle belge düzeninizi en iyi duruma getirin ve gelişmiş sunum için sorunsuz kitapçık yazdırmayı etkinleştirin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings/
---
## XpsSaveOptions.UseBookFoldPrintingSettings property

Belgenin kitapçık yazdırma düzeni kullanılarak kaydedilip kaydedilmeyeceğini belirten bir Boole değeri alır veya ayarlar, bu şekilde belirtilmişse[`MultiplePages`](../../../aspose.words/pagesetup/multiplepages/) .

```csharp
public bool UseBookFoldPrintingSettings { get; set; }
```

## Notlar

Bu seçenek belirtilirse,[`PageSet`](../../fixedpagesaveoptions/pageset/) kaydedilirken göz ardı edilir. Bu davranış MS Word ile eşleşir. Kitap katlama yazdırma ayarları sayfa düzeninde belirtilmemişse, bu seçeneğin hiçbir etkisi olmaz.

## Örnekler

Bir belgenin kitap katlaması şeklinde XPS formatına nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "XpsSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .XPS'e nasıl dönüştüreceğini değiştirmek için.
XpsSaveOptions xpsOptions = new XpsSaveOptions(SaveFormat.Xps);

// İçeriği düzenlemek için "UseBookFoldPrintingSettings" özelliğini "true" olarak ayarlayın
// çıktıda XPS'i kitapçık yapmak için kullanmamıza yardımcı olacak şekilde.
// XPS'i normal şekilde işlemek için "UseBookFoldPrintingSettings" özelliğini "false" olarak ayarlayın.
xpsOptions.UseBookFoldPrintingSettings = renderTextAsBookFold;

// Belgeyi kitapçık olarak oluşturuyorsak, "Çoklu Sayfalar"ı ayarlamalıyız
// tüm bölümlerin sayfa kurulumu nesnelerinin özellikleri "MultiplePagesType.BookFoldPrinting" olarak değiştirildi.
if (renderTextAsBookFold)
    foreach (Section s in doc.Sections)
    {
        s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
    }

// Bu belgeyi yazdırdığımızda, sayfaları üst üste koyarak bir kitapçığa dönüştürebiliriz
// yazıcıdan çıkıp ortadan katlanmak.
doc.Save(ArtifactsDir + "XpsSaveOptions.BookFold.xps", xpsOptions);
```

### Ayrıca bakınız

* class [XpsSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
