---
title: HtmlSaveOptions.ExportXhtmlTransitional
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. HTMLye veya MHTMLye kaydederken DOCTYPE bildiriminin yazıp yazmayacağını belirtir. Ne zamandoğru  belgede kök öğeden önce bir DOCTYPE bildirimi yazar. Varsayılan değerYANLIŞ. EPUB veya HTML5e kaydederken Html5  DOCTYPE bildirimi her zaman yazılır.
type: docs
weight: 280
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

HTML'ye veya MHTML'ye kaydederken DOCTYPE bildiriminin yazıp yazmayacağını belirtir. Ne zaman`doğru` , belgede kök öğeden önce bir DOCTYPE bildirimi yazar. Varsayılan değer:`YANLIŞ`. EPUB veya HTML5'e kaydederken (Html5 ) DOCTYPE bildirimi her zaman yazılır.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

### Notlar

Aspose.Words bu ayardan bağımsız olarak her zaman iyi biçimlendirilmiş HTML yazar.

Ne zaman`doğru`HTML çıktı belgesinin başlangıcı şöyle görünecektir:

Aspose.Words, XHTML 1.0 Transitional spesifikasyonuna ( ) göre XHTML çıktısı almayı hedefler ancak çıktı her zaman DTD'ye göre doğrulanmaz. Microsoft Word belgesi içindeki bazı yapıların XHTML şemasına göre doğrulama yapacak bir belgeyle eşleştirilmesi zor veya imkansızdır. Örneğin, XHTML iç içe geçmiş listelere izin vermez (UL, başka bir UL öğesinin içine yerleştirilemez), ancak Microsoft Word belgesinde çok düzeyli listeler oldukça sık görülür.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html 
      PUBLIC "-//W3C//DTD XHTML 1.0 Geçişli//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="tr" lang="tr">
```

### Örnekler

Belgeleri Xhtml 1.0 geçiş standardına dönüştürürken DOCTYPE başlığının nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    HtmlVersion = HtmlVersion.Xhtml,
    ExportXhtmlTransitional = showDoctypeDeclaration,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html", options);

// "ExportXhtmlTransitional" bayrağını "true" olarak ayarlamışsak, belgemiz yalnızca DOCTYPE bildirim başlığını içerecektir.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        "<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>\r\n" +
        "<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Transitional//EN\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd\">\r\n" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


