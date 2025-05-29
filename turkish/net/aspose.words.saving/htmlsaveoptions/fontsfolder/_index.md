---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: .NET için Aspose.Words
description: HTML dışa aktarımları için yazı tipi depolama alanını kolayca yönetmek, belge sunumunu ve erişilebilirliğini geliştirmek için HtmlSaveOptions FontsFolder özelliğini keşfedin.
type: docs
weight: 310
url: /tr/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Bir belgeyi HTML'ye aktarırken yazı tiplerinin kaydedildiği fiziksel klasörü belirtir. Varsayılan boş bir dizedir.

```csharp
public string FontsFolder { get; set; }
```

## Notlar

Birini kaydettiğinizde[`Document`](../../../aspose.words/document/) HTML formatında ve[`ExportFontResources`](../exportfontresources/) olarak ayarlandı`doğru` , Aspose.Words'ün belgede kullanılan yazı tiplerini bağımsız dosyalar olarak kaydetmesi gerekiyor. `FontsFolder` yazı tiplerinin nereye kaydedileceğini belirtmenize olanak tanır ve [`FontsFolderAlias`](../fontsfolderalias/) yazı tipi URI'lerinin nasıl oluşturulacağını belirtmeye olanak tanır.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız, Aspose.Words varsayılan olarak, yazı tiplerini belge dosyasının kaydedildiği klasöre kaydeder.`FontsFolder` Bu davranışı geçersiz kılmak için kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words fontları kaydedecek bir klasöre sahip değildir, ancak yine de fontları bir yere kaydetmesi gerekir. Bu durumda, erişilebilir bir klasör belirtmeniz gerekir `FontsFolder` özellik veya özel akışlar sağlayın via the[`FontSavingCallback`](../fontsavingcallback/) olay işleyicisi.

Belirtilen klasör`FontsFolder` mevcut değilse otomatik olarak oluşturulacaktır.

[`ResourceFolder`](../resourcefolder/) yazı tiplerinin kaydedileceği klasörü belirtmenin başka bir yoludur.

## Örnekler

Aspose.Words'ün bir belgeyi HTML'e kaydederken oluşturacağı harici olarak kaydedilen kaynaklar için klasörlerin ve klasör takma adlarının nasıl ayarlanacağını gösterir.

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
    FontsFolderAlias = "http://example.com/yazı tipleri",
    ImagesFolderAlias = "http://example.com/resimler",
    ResourceFolderAlias = "http://example.com/kaynaklar",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
