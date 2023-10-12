---
title: HtmlFixedSaveOptions.SaveFontFaceCssSeparately
second_title: Aspose.Words for .NET API Referansı
description: HtmlFixedSaveOptions mülk. Bayrak bir belge harici stil sayfasıyla kaydedilirken fontface CSS kurallarının ayrı bir fontFaces.css dosyasına yerleştirilmesi gerekip gerekmediğini belirtir yaniExportEmbeddedCss YANLIŞ . Varsayılan değerYANLIŞ  tüm CSS kuralları tek bir styles.css dosyasına yazılır.
type: docs
weight: 160
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/
---
## HtmlFixedSaveOptions.SaveFontFaceCssSeparately property

Bayrak, bir belge harici stil sayfasıyla kaydedilirken "@font-face" CSS kurallarının ayrı bir "fontFaces.css" dosyasına yerleştirilmesi gerekip gerekmediğini belirtir (yani,[`ExportEmbeddedCss`](../exportembeddedcss/) :`YANLIŞ` ). Varsayılan değer:`YANLIŞ` , tüm CSS kuralları tek bir "styles.css" dosyasına yazılır.

```csharp
public bool SaveFontFaceCssSeparately { get; set; }
```

### Notlar

Bu özelliği şuna ayarlıyoruz:`doğru` eski kodla uyumluluk için eski davranışı (ayrı dosyalar) geri yükler.

### Örnekler

CSS'nin ayrı bir dosyaya nasıl yerleştirileceğini ve tüm CSS sınıfı adlarına nasıl önek ekleneceğini gösterir.

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
* ad alanı [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* toplantı [Aspose.Words](../../../)


