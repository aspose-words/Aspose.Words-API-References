---
title: HtmlSaveOptions.ExportXhtmlTransitional
linktitle: ExportXhtmlTransitional
articleTitle: ExportXhtmlTransitional
second_title: .NET için Aspose.Words
description: HTML'nizi HtmlSaveOptions ExportXhtmlTransitional özelliğiyle optimize edin. HTML, MHTML ve EPUB formatlarında daha iyi uyumluluk için DOCTYPE bildirimlerini kontrol edin.
type: docs
weight: 280
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/
---
## HtmlSaveOptions.ExportXhtmlTransitional property

HTML veya MHTML'ye kaydederken DOCTYPE bildiriminin yazılıp yazılamayacağını belirtir. `doğru` , kök öğeden önce belgeye bir DOCTYPE bildirimi yazar. Varsayılan değer`YANLIŞ`. EPUB veya HTML5'e kaydederken (Html5 ) DOCTYPE bildirimi her zaman yazılır.

```csharp
public bool ExportXhtmlTransitional { get; set; }
```

## Notlar

Aspose.Words bu ayardan bağımsız olarak her zaman iyi biçimlendirilmiş HTML yazar.

Ne zaman`doğru`HTML çıktı belgesinin başlangıcı şu şekilde görünecektir:

Aspose.Words, XHTML 1.0 Transitional spesifikasyonuna göre XHTML çıktısı almayı hedefler, ancak çıktı her zaman DTD'ye göre doğrulanmaz. Microsoft Word belgesinin içindeki bazı yapıları XHTML şemasına göre doğrulanacak bir belgeye eşlemek zor veya imkansızdır. Örneğin, XHTML iç içe listeler (UL başka bir UL öğesinin içine yerleştirilemez) izin vermez, ancak Microsoft Word belgesinde çok düzeyli listeler oldukça sık görülür.

```csharp
<?xml version="1.0" encoding="utf-8" standalone="no" ?>
<!DOCTYPE html
      PUBLIC "-//W3C//DTD XHTML 1.0 Geçiş//TR"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-geçiş.dtd">
<html xmlns="http://www.w3.org/1999/xhtml" xml:lang="tr" lang="tr">
```

## Örnekler

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

// Belgemiz yalnızca "ExportXhtmlTransitional" bayrağını "true" olarak ayarladıysak bir DOCTYPE bildirim başlığı içerecektir.
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportXhtmlTransitional.html");
string newLine = Environment.NewLine;

if (showDoctypeDeclaration)
    Assert.True(outDocContents.Contains(
        $"<?xml version=\"1.0\" encoding=\"utf-8\" standalone=\"no\"?>{newLine}" +
        $"<!DOCTYPE html PUBLIC \"-//W3C//DTD XHTML 1.0 Geçiş//TR\" \"http://www.w3.org/TR/xhtml1/DTD/xhtml1-geçiş.dtd\">{newLine}" +
        "<html xmlns=\"http://www.w3.org/1999/xhtml\">"));
else
    Assert.True(outDocContents.Contains("<html>"));
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
