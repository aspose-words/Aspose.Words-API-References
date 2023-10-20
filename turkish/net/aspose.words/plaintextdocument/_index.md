---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words for .NET
description: Aspose.Words.PlainTextDocument sınıf. Belge içeriğinin düz metin gösteriminin çıkarılmasına izin verir C#'da.
type: docs
weight: 4440
url: /tr/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Belge içeriğinin düz metin gösteriminin çıkarılmasına izin verir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Metin Belgesiyle Çalışmak](https://docs.aspose.com/words/net/working-with-text-document/) dokümantasyon makalesi.

```csharp
public class PlainTextDocument
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | Bir akıştan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | Bir dosyadan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Bir akıştan düz metin belgesi oluşturur. Şifreleme şifresi gibi ek seçeneklerin belirtilmesine olanak tanır. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Bir dosyadan düz metin belgesi oluşturur. Şifreleme şifresi gibi ek seçeneklerin belirtilmesine olanak tanır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Alır[`BuiltInDocumentProperties`](./builtindocumentproperties/) belgenin. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Alır[`CustomDocumentProperties`](./customdocumentproperties/) belgenin. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Belgenin metin içeriğini bir dize olarak birleştirir. |

## Örnekler

Bir Microsoft Word belgesinin içeriğinin düz metin olarak nasıl yükleneceğini gösterir.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
