---
title: PlainTextDocument
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: Aspose.Words for .NET
description: PlainTextDocument inşaatçı. Bir dosyadan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument(*string*) {#constructor_2}

Bir dosyadan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar.

```csharp
public PlainTextDocument(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Metnin çıkarılacağı dosyanın adı. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge formatı tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve Aspose.Words geliştiricilerine bildirilmesi gerekiyor. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açılması için parola gerekiyor, ancak yanlış parola girdiniz. |
| ArgumentException | Dosyanın adı boş veya boş dize olamaz. |

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

* class [PlainTextDocument](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## PlainTextDocument(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_3}

Bir dosyadan düz metin belgesi oluşturur. Şifreleme şifresi gibi ek seçeneklerin belirtilmesine olanak tanır.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Metnin çıkarılacağı dosyanın adı. |
| loadOptions | LoadOptions | Belge yüklerken kullanılacak ek seçenekler. Olabilir`hükümsüz`. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge formatı tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve Aspose.Words geliştiricilerine bildirilmesi gerekiyor. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açılması için parola gerekiyor, ancak yanlış parola girdiniz. |
| ArgumentException | Dosyanın adı boş veya boş dize olamaz. |

## Örnekler

Şifrelenmiş bir Microsoft Word belgesinin içeriğinin düz metin olarak nasıl yükleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.LoadEncrypted.docx", loadOptions);

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream*) {#constructor}

Bir akıştan düz metin belgesi oluşturur. Dosya biçimini otomatik olarak algılar.

```csharp
public PlainTextDocument(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Metnin çıkarılacağı akış. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge formatı tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve Aspose.Words geliştiricilerine bildirilmesi gerekiyor. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açılması için parola gerekiyor, ancak yanlış parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış, okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akış, atılmış bir nesnedir. |

## Notlar

Belge akışın başında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler

Akış kullanılarak bir Microsoft Word belgesinin içeriğinin düz metin olarak nasıl yükleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx");

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStream.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Ayrıca bakınız

* class [PlainTextDocument](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## PlainTextDocument(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_1}

Bir akıştan düz metin belgesi oluşturur. Şifreleme şifresi gibi ek seçeneklerin belirtilmesine olanak tanır.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Metnin çıkarılacağı akış. |
| loadOptions | LoadOptions | Belge yüklerken kullanılacak ek seçenekler. Olabilir`hükümsüz`. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge formatı tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve Aspose.Words geliştiricilerine bildirilmesi gerekiyor. |
| IOException | Bir giriş/çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açılması için parola gerekiyor, ancak yanlış parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış, okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akış, atılmış bir nesnedir. |

## Notlar

Belge akışın başında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler

Akış kullanılarak şifrelenmiş bir Microsoft Word belgesinin içeriğinin düz metin olarak nasıl yükleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.Password = "MyPassword";

doc.Save(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

LoadOptions loadOptions = new LoadOptions();
loadOptions.Password = "MyPassword";

using (FileStream stream = new FileStream(ArtifactsDir + "PlainTextDocument.LoadFromStreamWithOptions.docx", FileMode.Open))
{
    PlainTextDocument plaintext = new PlainTextDocument(stream, loadOptions);

    Assert.AreEqual("Hello world!", plaintext.Text.Trim());
}
```

### Ayrıca bakınız

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [PlainTextDocument](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
