---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: .NET için Aspose.Words
description: HtmlFixedSaveOptions'ın ExportEmbeddedCss özelliğinin kusursuz stil için CSS'yi gömerek HTML belgelerinizi nasıl geliştirdiğini keşfedin. Web sayfalarınızı bugün optimize edin!
type: docs
weight: 40
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

CSS'nin (Basamaklı Stil Sayfası) Html belgesine yerleştirilip yerleştirilmeyeceğini belirtir.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## Örnekler

Bir belgeyi HTML'ye aktarırken CSS stil sayfalarının nerede saklanacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi html'e aktardığımızda, Aspose.Words aynı zamanda belgeyi biçimlendirmek için bir CSS stil sayfası da oluşturacaktır.
// "ExportEmbeddedCss" bayrağını "true" olarak ayarlayarak CSS stil sayfasını .css dosyasına kaydedin,
// ve <link> öğesini kullanarak html belgesinden dosyaya bağlantı verin.
// Bayrağı "false" olarak ayarlamak, CSS stil sayfasını Html belgesinin içine gömecektir.
// iki dosya yerine yalnızca bir dosya oluşturulacaktır.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.True(Regex.Match(outDocContents, "<style type=\"text/css\">").Success);
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success);
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
