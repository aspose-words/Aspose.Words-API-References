---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: .NET için Aspose.Words
description: HtmlFixedSaveOptions'daki ExportEmbeddedImages özelliğinin, Base64 formatındaki görüntüleri gömerek HTML belgelerinizi nasıl geliştirdiğini, dosya boyutunu yönetirken görsel kaliteyi nasıl iyileştirdiğini keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Görüntülerin Html belgesine Base64 biçiminde gömülmesi gerekip gerekmediğini belirtir. Bu bayrağı ayarlamanın çıktı Html dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Örnekler

Bir belgeyi HTML'e aktarırken resimlerin nereye kaydedileceğinin nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Gömülü resimler içeren bir belgeyi .html'ye aktardığımızda,
// Aspose.Words görselleri iki olası konuma yerleştirebilir.
// "ExportEmbeddedImages" bayrağını "true" olarak ayarlamak ham verileri depolayacaktır
// çıktı HTML belgesindeki tüm resimler için, <image> etiketlerinin "src" özniteliğinde.
// Bu bayrağı "false" olarak ayarlamak, her görüntü için yerel dosya sisteminde bir görüntü dosyası oluşturacaktır.
// ve tüm bu dosyaları ayrı bir klasörde saklayın.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedImages = exportImages
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages.html");

if (exportImages)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" src=\".+\" />").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedImages/image001.jpeg"));
    Assert.True(Regex.Match(outDocContents,
        "<img class=\"awimg\" style=\"left:0pt; top:0pt; width:493.1pt; height:300.55pt;\" " +
        "src=\"HtmlFixedSaveOptions[.]ExportEmbeddedImages/image001[.]jpeg\" />").Success);
}
```

### Ayrıca bakınız

* class [HtmlFixedSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
