---
title: Class SaveOutputParameters
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.SaveOutputParameters sınıf. Bu nesne bir belge kaydedildikten sonra arayan kişiye döndürülür ve kaydetme işlemi sırasında nin oluşturulduğu veya hesaplandığı ek bilgileri içerir. Arayan kişi bu nesneyi kullanabilir veya yok sayabilir.
type: docs
weight: 5590
url: /tr/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Bu nesne, bir belge kaydedildikten sonra arayan kişiye döndürülür ve kaydetme işlemi sırasında 'nin oluşturulduğu veya hesaplandığı ek bilgileri içerir. Arayan kişi bu nesneyi kullanabilir veya yok sayabilir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) dokümantasyon makalesi.

```csharp
public class SaveOutputParameters
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Kaydedilen belgenin türünü tanımlayan İçerik Türü dizesini (İnternet Medya Türü) döndürür. |

### Örnekler

Bir belgenin kaydetme işleminin çıktı parametrelerine nasıl erişileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Bir belgeyi kaydettikten sonra yeni oluşturulan çıktı belgesinin İnternet Medya Türüne (MIME türü) erişebiliriz.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Bu özellik kaydetme formatına bağlı olarak değişir.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


