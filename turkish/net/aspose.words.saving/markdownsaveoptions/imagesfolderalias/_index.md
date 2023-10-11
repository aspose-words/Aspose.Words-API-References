---
title: MarkdownSaveOptions.ImagesFolderAlias
second_title: Aspose.Words for .NET API Referansı
description: MarkdownSaveOptions mülk. Bir belgeye yazılan görüntü URIlerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan boş bir dizedir.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Bir belgeye yazılan görüntü URI'lerini oluşturmak için kullanılan klasörün adını belirtir. Varsayılan, boş bir dizedir.

```csharp
public string ImagesFolderAlias { get; set; }
```

### Notlar

Bir kaydettiğinizde[`Document`](../../../aspose.words/document/) içindeMarkdown format, Aspose.Words'ün belgeye gömülü tüm görselleri bağımsız dosyalar olarak kaydetmesi gerekiyor. [`ImagesFolder`](../imagesfolder/) görüntülerin nereye kaydedileceğini belirtmenize olanak tanır ve `ImagesFolderAlias` görüntü URI'lerinin nasıl oluşturulacağını belirlemeye olanak tanır.

Eğer`ImagesFolderAlias` boş bir dize değilse, Markdown'a yazılan görüntü URI'si şöyle olacaktır:ImagesFolderAlias + &lt;resim dosyası adı&gt;.

Eğer`ImagesFolderAlias` boş bir dize ise, Markdown'a yazılan görüntü URI'si şöyle olacaktır:ImagesFolder + &lt;resim dosyası adı&gt;.

Eğer`ImagesFolderAlias`ayarlandı '.' (nokta), diğer seçeneklere bakılmaksızın name görüntü dosyası Markdown'a yol olmadan yazılacaktır.

### Örnekler

Görüntü URI'lerini oluşturmak için kullanılan klasörün adının nasıl belirleneceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
Image image = Image.FromFile(ImageDir + "Logo.jpg");
builder.InsertImage(image);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Yerel dosya sisteminde içine bir klasör atamak için "ImagesFolder" özelliğini kullanın.
// Aspose.Words belgenin tüm bağlantılı görsellerini kaydedecektir.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Bu klasörü kullanmak için "ImagesFolderAlias" özelliğini kullanın
// resimler klasörünün adı yerine resim URI'lerini oluştururken.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

Görüntü URI'lerini (.NetStandard 2.0) oluşturmak için kullanılan klasörün adının nasıl belirtileceğini gösterir.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(bitmap);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Yerel dosya sisteminde içine bir klasör atamak için "ImagesFolder" özelliğini kullanın.
// Aspose.Words belgenin tüm bağlantılı görsellerini kaydedecektir.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Bu klasörü kullanmak için "ImagesFolderAlias" özelliğini kullanın
// resimler klasörünün adı yerine resim URI'lerini oluştururken.
saveOptions.ImagesFolderAlias = "http://example.com/images";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Ayrıca bakınız

* class [MarkdownSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../markdownsaveoptions/)
* toplantı [Aspose.Words](../../../)


