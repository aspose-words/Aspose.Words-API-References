---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: .NET için Aspose.Words
description: HTML belgenizin kenar boşluklarını özelleştirmek için HtmlFixedSaveOptions PageMargins özelliğini keşfedin. Hassas düzen kontrolü için değerleri noktalar halinde ayarlayın.
type: docs
weight: 130
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Bir HTML belgesindeki sayfaların etrafındaki kenar boşluklarını belirtir. Kenar boşluğu değeri puan olarak ölçülür ve 0'a eşit veya büyük olmalıdır. Varsayılan değer 10 puandır.

```csharp
public double PageMargins { get; set; }
```

## Notlar

Değerine bağlı[`PageHorizontalAlignment`](../pagehorizontalalignment/) mülk:

* Değer şuysa üst, alt ve sol sayfa kenar boşluklarını tanımlar:Left .
* Değer şuysa sayfanın üst, alt ve sağ kenar boşluklarını tanımlar:Right .
* Değer şuysa üst ve alt sayfa kenar boşluklarını tanımlar:Center .

## Örnekler

Bir belgeyi HTML olarak kaydederken sayfa kenar boşluklarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Document.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
{
    PageMargins = 15
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.PageMargins/styles.css");

Assert.True(Regex.Match(outDocContents,
    "[.]awpage { position:relative; border:solid 1pt black; margin:15pt auto 15pt auto; overflow:hidden; }").Success);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
