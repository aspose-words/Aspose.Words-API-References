---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: .NET için Aspose.Words
description: Belgeyi kaydettikten sonra önemli ayrıntıları sağlayan ve belge yönetimi deneyiminizi geliştiren Aspose.Words.Saving.SaveOutputParameters sınıfını keşfedin.
type: docs
weight: 6390
url: /tr/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Bu nesne, bir belge kaydedildikten sonra çağırana döndürülür ve kaydetme işlemi sırasında 'nin oluşturulduğu veya hesaplandığına dair ek bilgiler içerir. Çağıran bu nesneyi kullanabilir veya yoksayabilir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) belgeleme makalesi.

```csharp
public class SaveOutputParameters
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Kaydedilen belgenin türünü tanımlayan İçerik Türü dizesini (İnternet Medya Türü) döndürür. |

## Örnekler

Bir belgenin kaydetme işleminin çıktı parametrelerine nasıl erişileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Bir belgeyi kaydettikten sonra, yeni oluşturulan çıktı belgesinin İnternet Medya Türüne (MIME türü) erişebiliriz.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Bu özellik kayıt biçimine bağlı olarak değişir.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
