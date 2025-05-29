---
title: SaveOptions.TempFolder
linktitle: TempFolder
articleTitle: TempFolder
second_title: .NET için Aspose.Words
description: Geçici DOC ve DOCX dosyaları için bir klasör belirleyen SaveOptions TempFolder özelliğiyle belge kaydetme işleminizi optimize edin ve verimliliği artırın.
type: docs
weight: 140
url: /tr/net/aspose.words.saving/saveoptions/tempfolder/
---
## SaveOptions.TempFolder property

DOC veya DOCX dosyasına kaydederken kullanılan geçici dosyalar için klasörü belirtir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz.

```csharp
public string TempFolder { get; set; }
```

### istisnalar

| istisna | şart |
| --- | --- |
| OutOfMemoryException | Çok büyük bir belgeyi (binlerce sayfa) kaydediyorsanız ve/veya aynı anda birçok belgeyi işliyorsanız bu komutu kullanın. Kaydetme sırasında oluşan bellek artışı istisnaya neden olacak kadar önemli olabilir. |

## Notlar

Aspose.Words bir belgeyi kaydettiğinde, geçici dahili yapılar oluşturması gerekir. Varsayılan olarak, bu dahili yapılar bellekte oluşturulur ve bellek kullanımı, belge kaydedilirken kısa bir süre için yükselir. Kaydetme tamamlandığında, bellek boşaltılır ve çöp toplayıcı tarafından geri alınır.

Geçici bir klasörün belirtilmesi`TempFolder` Aspose.Words'ün dahili yapılarını bellek yerine geçici dosyalarda tutmasına neden olur. Kaydetme sırasında bellek kullanımını azaltır, ancak kaydetme performansını düşürür.

Klasör mevcut olmalı ve yazılabilir olmalıdır, aksi takdirde bir istisna atılacaktır.

Aspose.Words, kaydetme işlemi tamamlandığında tüm geçici dosyaları otomatik olarak siler.

## Örnekler

Bir belgeyi kaydederken bellek yerine sabit sürücünün nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Bir belgeyi kaydettiğimizde, kaydetme işlemi gerçekleşirken çeşitli öğeler geçici olarak bellekte saklanır.
// Bunun yerine yerel dosya sistemindeki geçici bir klasörü kullanmak için bu seçeneği kullanabiliriz.
// Bu da uygulamamızın bellek yükünü azaltacaktır.
DocSaveOptions options = new DocSaveOptions();
options.TempFolder = ArtifactsDir + "TempFiles";

// Belirtilen geçici klasör, kaydetme işleminden önce yerel dosya sisteminde mevcut olmalıdır.
Directory.CreateDirectory(options.TempFolder);

doc.Save(ArtifactsDir + "DocSaveOptions.TempFolder.doc", options);

// Klasör, yükleme işleminden kalan hiçbir içerik olmadan kalıcı olacaktır.
Assert.AreEqual(0, Directory.GetFiles(options.TempFolder).Length);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
