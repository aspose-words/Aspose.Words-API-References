---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: Aspose.Words for .NET
description: LoadOptions TempFolder mülk. Belgeyi okurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellikhükümsüz ve hiçbir geçici dosya kullanılmaz C#'da.
type: docs
weight: 150
url: /tr/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Belgeyi okurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz.

```csharp
public string TempFolder { get; set; }
```

## Notlar

Klasörün var olması ve yazılabilir olması gerekir, aksi takdirde bir istisna oluşturulacaktır.

Aspose.Words, okuma tamamlandığında tüm geçici dosyaları otomatik olarak siler.

## Örnekler

Geçici dosyalar kullanılarak bir belgenin nasıl yükleneceğini gösterir.

```csharp
// Böyle bir yaklaşımın bellek kullanımını azaltabileceğini ancak hızı düşürebileceğini unutmayın
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Dizinin var olduğundan emin olun ve yükleyin
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Bir belgeyi yüklerken bellek yerine sabit sürücünün nasıl kullanılacağını gösterir.

```csharp
// Bir belge yüklediğimizde, kaydetme işlemi gerçekleştiği için çeşitli öğeler geçici olarak bellekte saklanır.
// Bunun yerine yerel dosya sistemindeki geçici bir klasörü kullanmak için bu seçeneği kullanabiliriz,
// bu uygulamamızın hafıza yükünü azaltacaktır.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Belirtilen geçici klasörün yükleme işleminden önce yerel dosya sisteminde mevcut olması gerekir.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Klasör, yükleme işleminden kalan hiçbir içerik olmadan varlığını sürdürecek.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
