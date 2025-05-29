---
title: HtmlFixedSaveOptions.SaveFontFaceCssSeparately
linktitle: SaveFontFaceCssSeparately
articleTitle: SaveFontFaceCssSeparately
second_title: .NET için Aspose.Words
description: SaveFontFaceCssSeparately özelliğinin, daha temiz dışa aktarımlar için yazı tipi kurallarını ayrı bir dosyaya kaydederek belgenizin CSS yönetimini nasıl optimize ettiğini keşfedin.
type: docs
weight: 180
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/
---
## HtmlFixedSaveOptions.SaveFontFaceCssSeparately property

Bayrağı, bir belge harici stil sayfasıyla kaydedildiğinde (yani, "@font-face" CSS kurallarının ayrı bir "fontFaces.css" dosyasına yerleştirilip yerleştirilmeyeceğini belirtir.[`ExportEmbeddedCss`](../exportembeddedcss/) şudur`YANLIŞ` ). Varsayılan değer`YANLIŞ` , tüm CSS kuralları tek bir dosyaya yazılır "styles.css".

```csharp
public bool SaveFontFaceCssSeparately { get; set; }
```

## Notlar

Bu özelliği şu şekilde ayarlamak:`doğru` eski davranışı (ayrı dosyaları) eski kodla uyumluluk için geri yükler.

## Örnekler

CSS'nin ayrı bir dosyaya nasıl yerleştirileceğini ve tüm CSS sınıf adlarına bir önek nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Bookmarks.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    CssClassNamesPrefix = "myprefix",
    SaveFontFaceCssSeparately = true
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix.html");

Assert.True(Regex.Match(outDocContents,
    "<div class=\"myprefixdiv myprefixpage\" style=\"width:595[.]3pt; height:841[.]9pt;\">" +
    "<div class=\"myprefixdiv\" style=\"left:85[.]05pt; top:36pt; clip:rect[(]0pt,510[.]25pt,74[.]95pt,-85.05pt[)];\">" +
    "<span class=\"myprefixspan myprefixtext001\" style=\"font-size:11pt; left:294[.]73pt; top:0[.]36pt; line-height:12[.]29pt;\">").Success);

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.AddCssClassNamesPrefix/styles.css");

Assert.True(Regex.Match(outDocContents,
    ".myprefixdiv { position:absolute; } " +
    ".myprefixspan { position:absolute; white-space:pre; color:#000000; font-size:12pt; }").Success);
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
