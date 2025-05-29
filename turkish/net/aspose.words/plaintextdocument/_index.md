---
title: PlainTextDocument Class
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: .NET için Aspose.Words
description: Belgelerinizden düz metni zahmetsizce çıkarmak ve kullanmak için Aspose.Words.PlainTextDocument sınıfını keşfedin; böylece okunabilirliği ve işlemeyi geliştirin.
type: docs
weight: 5170
url: /tr/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Belgenin içeriğinin düz metin gösterimini çıkarmayı sağlar.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Metin Belgesiyle Çalışma](https://docs.aspose.com/words/net/working-with-text-document/) belgeleme makalesi.

```csharp
public class PlainTextDocument
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(*Stream*) | Bir akıştan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(*string*) | Bir dosyadan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Bir akıştan düz metin belgesi oluşturur. Şifreleme parolası gibi ek seçeneklerin belirtilmesine olanak tanır. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Bir dosyadan düz metin belgesi oluşturur. Şifreleme parolası gibi ek seçeneklerin belirtilmesine olanak tanır. |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Alır[`BuiltInDocumentProperties`](./builtindocumentproperties/) belgenin. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Alır[`CustomDocumentProperties`](./customdocumentproperties/) belgenin. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Belgenin metinsel içeriğini bir dize olarak birleştirilmiş olarak alır. |

## Örnekler

Microsoft Word belgesinin içeriğinin düz metin olarak nasıl yükleneceğini gösterir.

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
