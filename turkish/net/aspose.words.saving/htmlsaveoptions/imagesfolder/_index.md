---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ImagesFolder özelliğini keşfedin. Belgeleri HTML'e aktarırken görüntüleri kaydetmek için klasörü kolayca ayarlayın. İş akışınızı bugün hızlandırın!
type: docs
weight: 360
url: /tr/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Bir belgeyi HTML biçimine aktarırken görüntülerin kaydedileceği fiziksel klasörü belirtir. Varsayılan boş bir dizedir.

```csharp
public string ImagesFolder { get; set; }
```

## Notlar

Birini kaydettiğinizde[`Document`](../../../aspose.words/document/) HTML formatında, Aspose.Words'ün belgeye gömülü tüm resimleri bağımsız dosyalar olarak kaydetmesi gerekir.`ImagesFolder` görüntülerin nereye kaydedileceğini belirtmenize olanak tanır ve[`ImagesFolderAlias`](../imagesfolderalias/) görüntü URI'lerinin nasıl oluşturulacağını belirtmeye izin verir.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız, Aspose.Words varsayılan olarak, resimlerini belge dosyasının kaydedildiği klasöre kaydeder.`ImagesFolder` Bu davranışı geçersiz kılmak için kullanın.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'ün görüntüleri kaydedeceği bir klasörü yoktur, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, erişilebilir bir klasör belirtmeniz gerekir`ImagesFolder` özellik veya özel akışlar sağlayın via the[`ImageSavingCallback`](../imagesavingcallback/) olay işleyicisi.

Belirtilen klasör`ImagesFolder` mevcut değilse otomatik olarak oluşturulacaktır.

[`ResourceFolder`](../resourcefolder/) resimlerin kaydedileceği klasörü belirtmenin başka bir yoludur.

## Örnekler

Bağlantılı görsellerin .html olarak kaydedildikten sonra saklanacağı klasörün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Form alanlarını HTML giriş öğeleri yerine düz metin olarak dışa aktarmak için bir seçenek ayarlayın.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
