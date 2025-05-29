---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: .NET için Aspose.Words
description: Belgelerinizdeki resim URI'lerini kolayca yönetmek için MarkdownSaveOptions ImagesFolderAlias özelliğini keşfedin. Bu temel özellik ile iş akışınızı kolaylaştırın!
type: docs
weight: 90
url: /tr/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Bir belgeye yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Notlar

Birini kaydettiğinizde[`Document`](../../../aspose.words/document/) içindeMarkdown format, Aspose.Words'ün belgeye gömülü tüm görselleri bağımsız dosyalar olarak kaydetmesi gerekir. [`ImagesFolder`](../imagesfolder/) resimlerin nereye kaydedileceğini belirtmenize olanak tanır ve `ImagesFolderAlias` resim URI'lerinin nasıl oluşturulacağını belirtmeye olanak tanır.

Eğer`ImagesFolderAlias` boş bir dize değilse, Markdown'a yazılan görüntü URI'si şu şekilde olacaktır:ImagesFolderAlias + &lt;resim dosya adı&gt;.

Eğer`ImagesFolderAlias` boş bir dize ise, Markdown'a yazılan görüntü URI'si şu şekilde olacaktır:ImagesFolder + &lt;resim dosya adı&gt;.

Eğer`ImagesFolderAlias` '.' (nokta) olarak ayarlanırsa, görüntü dosyası adı diğer seçeneklerden bağımsız olarak yol olmaksızın Markdown'a yazılır.

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
