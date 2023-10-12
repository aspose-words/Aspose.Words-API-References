---
title: HtmlSaveOptions.ResolveFontNames
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Belgede kullanılan yazı tipi ailesi adlarının ye göre çözümlenip değiştirilmeyeceğini belirtirFontSettings HTML tabanlı formatlara yazılırken.
type: docs
weight: 410
url: /tr/net/aspose.words.saving/htmlsaveoptions/resolvefontnames/
---
## HtmlSaveOptions.ResolveFontNames property

Belgede kullanılan yazı tipi ailesi adlarının 'ye göre çözümlenip değiştirilmeyeceğini belirtir[`FontSettings`](../../../aspose.words/document/fontsettings/) HTML tabanlı formatlara yazılırken.

```csharp
public bool ResolveFontNames { get; set; }
```

### Notlar

Varsayılan olarak bu seçenek şu şekilde ayarlanmıştır:`YANLIŞ` ve yazı tipi ailesi adları, kaynak belgelerde belirtilen olarak HTML'ye yazılır. Yani,[`FontSettings`](../../../aspose.words/document/fontsettings/) göz ardı edilir ve yazı tipi ailesi adlarının çözümlenmesi veya ikame işlemi gerçekleştirilmez.

Bu seçenek olarak ayarlanmışsa`doğru` Aspose.Words'ün kullanım alanları[`FontSettings`](../../../aspose.words/document/fontsettings/) bir kaynak belgede belirtilen her yazı tipi ailesi adını mevcut bir yazı tipi ailesinin adına çözümlemek ve gerektiğinde yazı tipi değişimini gerçekleştirmek.

### Örnekler

Tüm yazı tipi adlarının HTML'ye yazılmadan önce nasıl çözümleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Missing font.docx");

// Bu belge elimizde olmayan bir yazı tipini adlandıran metin içeriyor.
Assert.NotNull(doc.FontInfos["28 Days Later"]);

// Bu yazı tipini almamızın bir yolu yoksa ve tüm metni görüntüleyebilmek istiyorsak
// bu belgedeki çıktı HTML'sinde onu başka bir yazı tipiyle değiştirebiliriz.
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
    // Varsayılan olarak bu seçenek 'Yanlış' olarak ayarlıdır ve Aspose.Words, kaynak belgede belirtildiği gibi yazı tipi adlarını yazar
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
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


