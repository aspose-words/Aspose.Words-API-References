---
title: HtmlSaveOptions.FontsFolder
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Bir belgeyi HTMLye aktarırken yazı tiplerinin kaydedildiği fiziksel klasörü belirtir. Varsayılan boş bir dizedir.
type: docs
weight: 310
url: /tr/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Bir belgeyi HTML'ye aktarırken yazı tiplerinin kaydedildiği fiziksel klasörü belirtir. Varsayılan, boş bir dizedir.

```csharp
public string FontsFolder { get; set; }
```

### Notlar

Bir kaydettiğinizde[`Document`](../../../aspose.words/document/) HTML formatında ve[`ExportFontResources`](../exportfontresources/) şu şekilde ayarlandı`doğru` , Aspose.Words'ün belgede kullanılan yazı tiplerini bağımsız dosyalar olarak kaydetmesi gerekir. `FontsFolder` yazı tiplerinin nereye kaydedileceğini ve belirtmenizi sağlar[`FontsFolderAlias`](../fontsfolderalias/) yazı tipi URI'lerinin nasıl oluşturulacağını belirlemeye olanak tanır.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız, Aspose.Words varsayılan olarak yazı tiplerini belge dosyasının kaydedildiği klasöre kaydeder. Kullanmak`FontsFolder` Bu davranışı geçersiz kılmak için .

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'te fontların kaydedileceği bir klasör yoktur, ancak yine de fontları bir yere kaydetmesi gerekir. Bu durumda, erişilebilir bir klasör belirtmeniz gerekir.`FontsFolder` özelliği veya aracılığıyla özel akışlar sağlayın[`FontSavingCallback`](../fontsavingcallback/) olay işleyicisi.

tarafından belirtilen klasör ise`FontsFolder` mevcut değilse otomatik olarak oluşturulacaktır.

[`ResourceFolder`](../resourcefolder/) yazı tiplerinin kaydedileceği klasörü belirtmenin başka bir yoludur.

### Örnekler

Aspose.Words'ün bir belgeyi HTML'ye kaydederken oluşturacağı harici olarak kaydedilen kaynaklar için klasörlerin ve klasör takma adlarının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://example.com/fonts",
    ImagesFolderAlias = "http://example.com/images",
    ResourceFolderAlias = "http://example.com/resources",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


