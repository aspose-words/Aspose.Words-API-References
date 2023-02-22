---
title: LoadOptions.TempFolder
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellikhükümsüz ve hiçbir geçici dosya kullanılmaz.
type: docs
weight: 150
url: /tr/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Belge okunurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz.

```csharp
public string TempFolder { get; set; }
```

### Notlar

Klasör var olmalı ve yazılabilir olmalıdır, aksi takdirde bir istisna atılır.

Aspose.Words, okuma tamamlandığında tüm geçici dosyaları otomatik olarak siler.

### Örnekler

Geçici dosyalar kullanılarak bir belgenin nasıl yükleneceğini gösterir.

```csharp
// Böyle bir yaklaşımın bellek kullanımını azaltabileceğini ancak hızı düşürdüğünü unutmayın.
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Dizinin var olduğundan ve yüklendiğinden emin olun
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Belge yüklerken bellek yerine sabit sürücünün nasıl kullanılacağını gösterir.

```csharp
// Bir belge yüklediğimizde, kaydetme işlemi gerçekleştiği için çeşitli elemanlar geçici olarak bellekte saklanır.
// Bunun yerine yerel dosya sisteminde geçici bir klasör kullanmak için bu seçeneği kullanabiliriz,
// uygulamamızın bellek yükünü azaltacak.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Belirtilen geçici klasör, yükleme işleminden önce yerel dosya sisteminde bulunmalıdır.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Klasör, yükleme işleminden kalan içerik olmadan devam edecek.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


