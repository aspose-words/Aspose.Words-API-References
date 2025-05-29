---
title: HtmlSaveOptions.ResolveFontNames
linktitle: ResolveFontNames
articleTitle: ResolveFontNames
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ResolveFontNames özelliğinin HTML çıktılarında doğru yazı tipi değişimlerini sağlayarak belge biçimlendirmesini nasıl geliştirdiğini keşfedin.
type: docs
weight: 430
url: /tr/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Belgede kullanılan yazı tipi aile adlarının çözümlenip çözümlenmeyeceğini ve 'ye göre değiştirilip değiştirilmeyeceğini belirtir[`FontSettings`](../../../aspose.words/document/fontsettings/) HTML tabanlı formatlara yazıldığında.

```csharp
public bool ResolveFontNames { get; set; }
```

## Notlar

Varsayılan olarak bu seçenek şu şekilde ayarlanmıştır:`YANLIŞ` ve font aile adları HTML'ye kaynak belgelerde belirtilen olarak yazılır. Yani,[`FontSettings`](../../../aspose.words/document/fontsettings/) göz ardı edilir ve font ailesi adlarının çözümü veya değiştirilmesi yapılmaz.

Bu seçenek şu şekilde ayarlanırsa:`doğru` , Aspose.Words kullanır[`FontSettings`](../../../aspose.words/document/fontsettings/) Kaynak belgede belirtilen her bir font ailesi adının, mevcut bir font ailesinin adına dönüştürülmesi için gerekli olduğu takdirde, font değişiminin gerçekleştirilmesi.

## Örnekler

Tüm font adlarının HTML'e yazılmadan önce nasıl çözümleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Bu belge, sahip olmadığımız bir yazı tipini adlandıran metin içeriyor.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Bu yazı tipini elde etmenin bir yolu yoksa ve tüm metni görüntülemek istiyorsak
// bu belgede çıktı HTML'inde, bunu başka bir yazı tipiyle değiştirebiliriz.
FontSettings fontSettings = new FontSettings
{
    SubstitutionSettings =
    {
        DefaultFontSubstitution =
        {
            DefaultFontName = "Arial",
            Enabled = true
        }
    }
};

doc.FontSettings = fontSettings;

HtmlSaveOptions saveOptions = new HtmlSaveOptions(SaveFormat.Html)
{
    // Varsayılan olarak, bu seçenek 'False' olarak ayarlanır ve Aspose.Words, yazı tipi adlarını kaynak belgede belirtildiği gibi yazar
    ResolveFontNames = resolveFontNames
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ResolveFontNames.html");

Assert.True(resolveFontNames
    ? Regex.Match(outDocContents, "<span style=\"font-family:Arial\">").Success
    : Regex.Match(outDocContents, "<span style=\"font-family:\'28 Days Later\'\">").Success);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
