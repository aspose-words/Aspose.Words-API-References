---
title: SaveOptions.TempFolder
second_title: Aspose.Words for .NET API Referansı
description: SaveOptions mülk. Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellikhükümsüz ve hiçbir geçici dosya kullanılmaz.
type: docs
weight: 150
url: /tr/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz.

```csharp
public string TempFolder { get; set; }
```

### Notlar

Aspose.Words bir belgeyi kaydettiğinde, geçici dahili yapılar oluşturması gerekir. Varsayılan olarak, bu dahili yapılar bellekte oluşturulur ve belge kaydedilirken bellek kullanımı kısa bir süre için yükselir. Kaydetme işlemi tamamlandığında, bellek boşaltılır ve çöp toplayıcı tarafından geri alınır.

Çok büyük bir belgeyi (binlerce sayfa) kaydediyorsanız ve/veya aynı anda birçok belgeyi işliyorsanız, , o zaman kaydetme sırasındaki bellek artışı sistemin atmasına neden olacak kadar önemli olabilir.OutOfMemoryException . kullanarak geçici bir klasör belirtme`TempFolder` Aspose.Words'ün dahili yapıları bellek yerine geçici dosyalarında tutmasına neden olur. Kaydetme sırasında bellek kullanımını azaltır ancak kaydetme performansını düşürür.

Klasör var olmalı ve yazılabilir olmalıdır, aksi takdirde bir istisna atılır.

Aspose.Words, kaydetme işlemi tamamlandığında tüm geçici dosyaları otomatik olarak siler.

### Örnekler

Bir belgeyi kaydederken bellek yerine sabit sürücünün nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi kaydettiğimizde, kaydetme işlemi gerçekleşirken çeşitli elemanlar geçici olarak bellekte saklanır.
// Bunun yerine yerel dosya sisteminde geçici bir klasör kullanmak için bu seçeneği kullanabiliriz,
// uygulamamızın bellek yükünü azaltacak.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Belirtilen geçici klasör, kaydetme işleminden önce yerel dosya sisteminde bulunmalıdır.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Klasör, yükleme işleminden kalan içerik olmadan devam edecek.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../saveoptions/)
* toplantı [Aspose.Words](../../../)


