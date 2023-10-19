---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words for .NET
description: HtmlFixedSaveOptions ExportEmbeddedCss mülk. CSSnin Basamaklı Stil Sayfası Html belgesine gömülmesi gerekip gerekmediğini belirtir C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

CSS'nin (Basamaklı Stil Sayfası) Html belgesine gömülmesi gerekip gerekmediğini belirtir.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## Örnekler

Bir belgeyi Html'ye aktarırken CSS stil sayfalarının nerede saklanacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi html'ye aktardığımızda Aspose.Words ayrıca belgeyi biçimlendirmek için bir CSS stil sayfası oluşturacaktır.
// "ExportEmbeddedCss" bayrağını "true" olarak ayarlamak, CSS stil sayfasını bir .css dosyasına kaydedin,
// ve <link> kullanarak html belgesinden dosyaya bağlantı verin eleman.
// Bayrağı "yanlış" olarak ayarlamak CSS stil sayfasını Html belgesinin içine yerleştirecektir,
// bu iki yerine yalnızca bir dosya oluşturacaktır.
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
