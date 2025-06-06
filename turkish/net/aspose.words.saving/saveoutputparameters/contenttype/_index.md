---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: .NET için Aspose.Words
description: Kaydedilmiş belgeleriniz için İnternet Medya Türünü sağlayan ve doğru dosya tanımlamasını garantileyen SaveOutputParameters ContentType özelliğini keşfedin.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Kaydedilen belgenin türünü tanımlayan İçerik Türü dizesini (İnternet Medya Türü) döndürür.

```csharp
public string ContentType { get; }
```

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

* class [SaveOutputParameters](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
