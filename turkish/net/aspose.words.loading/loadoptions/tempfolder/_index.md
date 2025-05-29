---
title: LoadOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: .NET için Aspose.Words
description: LoadOptions' TempFolder özelliğiyle belge okumayı optimize edin. Verimli işleme ve gelişmiş performans için geçici dosyaları kolayca yönetin.
type: docs
weight: 150
url: /tr/net/aspose.words.loading/loadoptions/tempfolder/
---
## LoadOptions.TempFolder property

Belgeyi okurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz.

```csharp
public string TempFolder { get; set; }
```

## Notlar

Klasör mevcut olmalı ve yazılabilir olmalıdır, aksi takdirde bir istisna atılacaktır.

Okuma işlemi tamamlandığında Aspose.Words tüm geçici dosyaları otomatik olarak siler.

## Örnekler

Geçici dosyalar kullanılarak bir belgenin nasıl yükleneceğini gösterir.

```csharp
// Bu tür bir yaklaşımın bellek kullanımını azaltabileceğini ancak hızı düşürdüğünü unutmayın
LoadOptions loadOptions = new LoadOptions();
loadOptions.TempFolder = @"C:\TempFolder\";

// Dizinin mevcut olduğundan emin olun ve yükleyin
Directory.CreateDirectory(loadOptions.TempFolder);

Document doc = new Document(MyDir + "Document.docx", loadOptions);
```

Bir belge yüklenirken bellek yerine sabit sürücünün nasıl kullanılacağını gösterir.

```csharp
// Bir belgeyi yüklediğimizde, kaydetme işlemi gerçekleştiğinde çeşitli öğeler geçici olarak bellekte saklanır.
// Bunun yerine yerel dosya sistemindeki geçici bir klasörü kullanmak için bu seçeneği kullanabiliriz.
// Bu da uygulamamızın bellek yükünü azaltacaktır.
LoadOptions options = new LoadOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Belirtilen geçici klasör, yükleme işleminden önce yerel dosya sisteminde mevcut olmalıdır.
Directory.CreateDirectory(options.TempFolder);

Document doc = new Document(MyDir + "Document.docx", options);

// Klasör, yükleme işleminden kalan hiçbir içerik olmadan kalıcı olacaktır.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Ayrıca bakınız

* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
