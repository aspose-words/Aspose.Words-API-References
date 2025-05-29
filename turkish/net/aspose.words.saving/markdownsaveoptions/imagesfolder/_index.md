---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: .NET için Aspose.Words
description: MarkdownSaveOptions ImagesFolder özelliğinin, Markdown formatındaki görüntüleri kaydetmek için ideal klasörü belirleyerek belge dışa aktarımlarınızı nasıl geliştirdiğini keşfedin.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Bir belgeyi dışa aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir. Markdown biçim. Varsayılan boş bir dizedir.

```csharp
public string ImagesFolder { get; set; }
```

## Notlar

Bir dosyayı kaydettiğinizde[`Document`](../../../aspose.words/document/) içindeMarkdownformat, Aspose.Words'ün belgeye gömülü tüm görselleri bağımsız dosyalar olarak kaydetmesi gerekir. `ImagesFolder` resimlerin nereye kaydedileceğini belirtmenize olanak tanır.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız, Aspose.Words varsayılan olarak görüntüleri belge dosyasının kaydedildiği aynı klasöre kaydeder.`ImagesFolder` bu davranışı geçersiz kılmak için.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'ün görüntüleri kaydedeceği bir klasörü yoktur, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, erişilebilir bir klasör belirtmeniz gerekir.`ImagesFolder` mülk.

Belirtilen klasör`ImagesFolder` mevcut değilse, otomatik olarak oluşturulacaktır.

## Örnekler

Görüntü URI'lerini oluşturmak için kullanılan klasörün adının nasıl belirtileceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Yerel dosya sistemindeki bir klasörü atamak için "ImagesFolder" özelliğini kullanın.
// Aspose.Words belgenin tüm bağlantılı resimlerini kaydedecektir.
saveOptions.ImagesFolder = imagesFolder;
// Bu klasörü kullanmak için "ImagesFolderAlias" özelliğini kullanın
// images klasörünün adı yerine image URI'leri oluşturulurken.
saveOptions.ImagesFolderAlias = "http://example.com/resimler";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Ayrıca bakınız

* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
