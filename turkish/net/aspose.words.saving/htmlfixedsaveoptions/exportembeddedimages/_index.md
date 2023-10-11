---
title: HtmlFixedSaveOptions.ExportEmbeddedImages
second_title: Aspose.Words for .NET API Referansı
description: HtmlFixedSaveOptions mülk. Görüntülerin Html belgesine Base64 biçiminde gömülmesi gerekip gerekmediğini belirtir. Bu bayrağın ayarlanmasının çıktı Html dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/
---
## HtmlFixedSaveOptions.ExportEmbeddedImages property

Görüntülerin Html belgesine Base64 biçiminde gömülmesi gerekip gerekmediğini belirtir. Bu bayrağın ayarlanmasının çıktı Html dosyasının boyutunu önemli ölçüde artırabileceğini unutmayın.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

### Örnekler

Bir belgeyi Html'ye aktarırken görüntülerin nerede saklanacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Gömülü görseller içeren bir belgeyi .html'ye aktardığımızda,
// Aspose.Words görüntüleri iki olası konuma yerleştirebilir.
// "ExportEmbeddedImages" bayrağını "true" olarak ayarlamak ham verileri depolayacaktır
// çıktı HTML belgesindeki tüm görüntüler için, <image> öğesinin "src" özelliğinde; Etiketler.
// Bu bayrağın "yanlış" olarak ayarlanması, yerel dosya sisteminde her görüntü için bir görüntü dosyası oluşturacaktır,
// ve tüm bu dosyaları ayrı bir klasörde saklıyoruz.
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
* ad alanı [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* toplantı [Aspose.Words](../../../)


