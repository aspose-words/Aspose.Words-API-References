---
title: MarkdownSaveOptions.ImagesFolder
second_title: Aspose.Words for .NET API Referansı
description: MarkdownSaveOptions mülk. Bir belgeyi ye aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir.Markdown biçim. Varsayılan boş bir dizedir.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Bir belgeyi 'ye aktarırken görüntülerin kaydedildiği fiziksel klasörü belirtir.Markdown biçim. Varsayılan boş bir dizedir.

```csharp
public string ImagesFolder { get; set; }
```

### Notlar

Bir dosyayı kaydettiğinizde[`Document`](../../../aspose.words/document/) içindeMarkdownformat, Aspose.Words'ün belgeye gömülü tüm görselleri bağımsız dosyalar olarak kaydetmesi gerekiyor. `ImagesFolder` görüntülerin nereye kaydedileceğini belirtmenizi sağlar.

Bir belgeyi bir dosyaya kaydederseniz ve bir dosya adı sağlarsanız Aspose.Words, varsayılan olarak görüntüleri belge dosyasının kaydedildiği klasöre kaydeder. Kullanmak`ImagesFolder` bu davranışı geçersiz kılmak için.

Bir belgeyi bir akışa kaydederseniz, Aspose.Words'de görüntülerin kaydedileceği bir klasör yoktur, ancak yine de görüntüleri bir yere kaydetmesi gerekir. Bu durumda, içinde erişilebilir bir klasör belirtmeniz gerekir.`ImagesFolder` özellik.

Eğer belirtilen klasör`ImagesFolder` mevcut değil, otomatik olarak oluşturulacak.

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


