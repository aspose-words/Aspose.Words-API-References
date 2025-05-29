---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: .NET için Aspose.Words
description: HtmlSaveOptions' ExportCidUrlsForMhtmlResources'un resimler, yazı tipleri ve CSS için CID URL'lerini etkinleştirerek MHTML belgelerini nasıl geliştirdiğini keşfedin. Varsayılan, false.
type: docs
weight: 110
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

MHTML belgelerinde yer alan kaynaklara (görüntüler, yazı tipleri, CSS) başvurmak için CID (İçerik Kimliği) URL'lerinin kullanılıp kullanılmayacağını belirtir. Varsayılan değer`YANLIŞ` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## Notlar

Bu seçenek yalnızca MHTML'ye kaydedilen belgeleri etkiler.

Varsayılan olarak, MHTML belgelerindeki kaynaklara dosya adına göre başvurulur (örneğin, "image.png"), which MIME parçalarının "Content-Location" başlıklarıyla eşleştirilir.

Bu seçenek, kaynak dosyalarına yapılan başvuruların CID (Content-ID) URL'leri (örneğin, "cid:image.png") olarak yazıldığı ve "Content-ID" başlıklarıyla eşleştirildiği alternatif bir yöntemi etkinleştirir.

Teoride, iki referans yöntemi arasında bir fark olmamalı ve her ikisi de herhangi bir tarayıcıda veya posta aracısında sorunsuz çalışmalıdır. Ancak pratikte, bazı aracılar kaynakları dosya adına göre getirmeyi başaramaz. Eğer tarayıcınız veya posta aracınız bir MTHML belgesinde bulunan kaynakları yüklemeyi reddederse (görüntüleri göstermiyorsa veya CSS stillerini yüklemiyorsa), belgeyi CID URL'leriyle dışa aktarmayı deneyin.

## Örnekler

Çıkış MHTML belgeleri için içerik kimliklerinin nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bu bayrağın ayarlanması "İçerik-Konum" etiketlerini değiştirecektir
// Giriş belgesindeki her kaynak için "Content-ID" etiketleriyle.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Mhtml)
{
    ExportCidUrlsForMhtmlResources = exportCidUrlsForMhtmlResources,
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ContentIdUrls.mht");

if (exportCidUrlsForMhtmlResources)
{
    Assert.True(outDocContents.Contains("Content-ID: <document.html>"));
    Assert.True(outDocContents.Contains("<link href=3D\"cid:styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('cid:arib=\r\nlk.ttf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"cid:image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
else
{
    Assert.True(outDocContents.Contains("Content-Location: document.html"));
    Assert.True(outDocContents.Contains("<link href=3D\"styles.css\" type=3D\"text/css\" rel=3D\"stylesheet\" />"));
    Assert.True(outDocContents.Contains("@font-face { font-family:'Arial Black'; font-weight:bold; src:url('ariblk.t=\r\ntf') }"));
    Assert.True(outDocContents.Contains("<img src=3D\"image.003.jpeg\" width=3D\"350\" height=3D\"180\" alt=3D\"\" />"));
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
