---
title: SaveOptions.TempFolder
second_title: Aspose.Words for .NET API Referansı
description: SaveOptions mülk. Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellikhükümsüz ve hiçbir geçici dosya kullanılmaz.
type: docs
weight: 140
url: /tr/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

Bir DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve hiçbir geçici dosya kullanılmaz.

```csharp
public string TempFolder { get; set; }
```

### Notlar

Aspose.Words bir belgeyi kaydettiğinde geçici iç yapılar oluşturması gerekir. Varsayılan olarak, bu dahili yapılar bellekte oluşturulur ve belge kaydedilirken bellek kullanımı kısa bir süreliğine yükselir. Kaydetme tamamlandığında bellek serbest bırakılır ve çöp toplayıcı tarafından geri alınır.

Çok büyük bir belge (binlerce sayfa) kaydediyorsanız ve/veya aynı anda birçok belgeyi işliyorsanız, bu durumda kaydetme sırasındaki bellek artışı, sistemin hata vermesine neden olacak kadar önemli olabilir.OutOfMemoryException . Kullanarak geçici bir klasör belirtme`TempFolder` Aspose.Words'ün dahili yapıları bellek yerine geçici dosyalarda tutmasına neden olur. Kaydetme sırasında bellek kullanımını azaltır ancak kaydetme performansını düşürür.

Klasörün var olması ve yazılabilir olması gerekir, aksi takdirde bir istisna oluşturulacaktır.

Aspose.Words, kaydetme işlemi tamamlandığında tüm geçici dosyaları otomatik olarak siler.

### Örnekler

Bir belgeyi kaydederken bellek yerine sabit sürücünün nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi kaydettiğimizde, kaydetme işlemi devam ederken çeşitli öğeler geçici olarak bellekte saklanır.
// Bunun yerine yerel dosya sistemindeki geçici bir klasörü kullanmak için bu seçeneği kullanabiliriz,
// bu uygulamamızın hafıza yükünü azaltacaktır.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Belirtilen geçici klasörün kaydetme işleminden önce yerel dosya sisteminde mevcut olması gerekir.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Klasör, yükleme işleminden kalan hiçbir içerik olmadan varlığını sürdürecek.
Assert.That(Directory.GetFiles(options.TempFolder), Is.Empty);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../saveoptions/)
* toplantı [Aspose.Words](../../../)


