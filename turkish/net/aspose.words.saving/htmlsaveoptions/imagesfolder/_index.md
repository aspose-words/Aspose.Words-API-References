---
title: HtmlSaveOptions.ImagesFolder
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Bir belgeyi HTML biçimine dışa aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılan boş bir dizedir.
type: docs
weight: 360
url: /tr/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Bir belgeyi HTML biçimine dışa aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir. Varsayılan, boş bir dizedir.

```csharp
public string ImagesFolder { get; set; }
```

### Notlar

Bir kaydettiğinizde[`Document`](../../../aspose.words/document/) HTML formatında Aspose.Words'ün belgeye gömülü tüm görsellerini bağımsız dosyalar olarak kaydetmesi gerekir.`ImagesFolder` görüntülerin nereye kaydedileceğini belirtmenize ve[`ImagesFolderAlias`](../imagesfolderalias/) , görüntü URI'lerinin nasıl oluşturulacağını belirtmeye olanak tanır.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntülerini belge dosyasının kaydedildiği klasöre kaydeder. Kullanmak`ImagesFolder` Bu davranışı geçersiz kılmak için .

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'de görüntülerin kaydedileceği bir klasör yoktur ( ), ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, erişilebilir bir klasör belirtmeniz gerekir.`ImagesFolder` özelliği veya aracılığıyla özel akışlar sağlayın[`ImageSavingCallback`](../imagesavingcallback/) olay işleyicisi.

tarafından belirtilen klasör ise`ImagesFolder` mevcut değilse otomatik olarak oluşturulacaktır.

[`ResourceFolder`](../resourcefolder/) görüntülerin kaydedileceği klasörü belirtmenin başka bir yoludur.

### Örnekler

Bağlantılı görsellerin .html'ye kaydedildikten sonra saklanacağı klasörün nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Form alanlarını HTML giriş öğeleri yerine düz metin olarak dışa aktarmak için bir seçenek belirleyin.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


