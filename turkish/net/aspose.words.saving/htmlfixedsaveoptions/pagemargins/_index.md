---
title: HtmlFixedSaveOptions.PageMargins
linktitle: PageMargins
articleTitle: PageMargins
second_title: Aspose.Words for .NET
description: HtmlFixedSaveOptions PageMargins mülk. Bir HTML belgesindeki sayfaların etrafındaki kenar boşluklarını belirtir. Kenar boşlukları değeri nokta cinsinden ölçülür ve 0a eşit veya daha büyük olmalıdır. Varsayılan değer 10 puntodur C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/pagemargins/
---
## HtmlFixedSaveOptions.PageMargins property

Bir HTML belgesindeki sayfaların etrafındaki kenar boşluklarını belirtir. Kenar boşlukları değeri nokta cinsinden ölçülür ve 0'a eşit veya daha büyük olmalıdır. Varsayılan değer 10 puntodur.

```csharp
public double PageMargins { get; set; }
```

## Notlar

Değerine bağlıdır[`PageHorizontalAlignment`](../pagehorizontalalignment/) mülk:

* Değer şu şekildeyse üst, alt ve sol sayfa kenar boşluklarını tanımlar:Left .
* Değer şu şekildeyse üst, alt ve sağ sayfa kenar boşluklarını tanımlarRight .
* Değer şu şekildeyse üst ve alt sayfa kenar boşluklarını tanımlar:Center .

## Örnekler

Bir belgeyi HTML'ye kaydederken sayfa kenar boşluklarının nasıl ayarlanacağını gösterir.

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
