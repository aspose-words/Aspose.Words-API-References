---
title: HtmlSaveOptions.ExportCidUrlsForMhtmlResources
linktitle: ExportCidUrlsForMhtmlResources
articleTitle: ExportCidUrlsForMhtmlResources
second_title: Aspose.Words for .NET
description: HtmlSaveOptions ExportCidUrlsForMhtmlResources mülk. MHTML belgelerinde bulunan kaynaklara resimler yazı tipleri CSS başvurmak için CID İçerik Kimliği URLlerinin kullanılıp kullanılmayacağını belirtir. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 110
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/
---
## HtmlSaveOptions.ExportCidUrlsForMhtmlResources property

MHTML belgelerinde bulunan kaynaklara (resimler, yazı tipleri, CSS) başvurmak için CID (İçerik Kimliği) URL'lerinin kullanılıp kullanılmayacağını belirtir. Varsayılan değer:`YANLIŞ` .

```csharp
public bool ExportCidUrlsForMhtmlResources { get; set; }
```

## Notlar

Bu seçenek yalnızca MHTML'ye kaydedilen belgeleri etkiler.

Varsayılan olarak, MHTML belgelerindeki kaynaklara dosya adıyla başvurulur (örneğin, "image.png") ve bu , MIME bölümlerinin "İçerik-Konum" başlıklarıyla eşleştirilir.

Bu seçenek, kaynak dosyalarına yapılan referansların CID (Content-ID) URL'leri (örneğin, "cid:image.png") olarak yazıldığı ve "Content-ID" başlıklarıyla eşleştirildiği alternatif bir yöntemi etkinleştirir.

Teorik olarak, iki referanslama yöntemi arasında hiçbir fark olmamalıdır ve her ikisi de herhangi bir tarayıcıda veya posta aracısında fine çalışmalıdır. Ancak uygulamada bazı aracılar kaynakları dosya adına göre getirmede başarısız olur. Eğer tarayıcınız veya posta aracınız bir MTHML belgesinde yer alan kaynakları yüklemeyi reddediyorsa (resimleri göstermiyor veya CSS stillerini yüklemiyorsa), belgeyi CID URL'leri ile dışa aktarmayı deneyin.

## Örnekler

Çıkış MHTML belgeleri için içerik kimliklerinin nasıl etkinleştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bu bayrağın ayarlanması "İçerik-Konum" etiketlerinin yerini alacaktır
// giriş belgesindeki her kaynak için "Content-ID" etiketleriyle.
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
