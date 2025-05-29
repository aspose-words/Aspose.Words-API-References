---
title: PlainTextDocument
linktitle: PlainTextDocument
articleTitle: PlainTextDocument
second_title: .NET için Aspose.Words
description: PlainTextDocument oluşturucumuzla zahmetsizce düz metin belgeleri oluşturun. Sorunsuz entegrasyon için otomatik dosya biçimi algılamanın keyfini çıkarın!
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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve bu durum Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Giriş/Çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açmak için bir parola gerekiyor, ancak yanlış bir parola girdiniz. |
| ArgumentException | Dosyanın adı null veya boş dize olamaz. |

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

* class [PlainTextDocument](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## PlainTextDocument(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/)*) {#constructor_3}

Bir dosyadan düz metin belgesi oluşturur. Şifreleme parolası gibi ek seçeneklerin belirtilmesine olanak tanır.

```csharp
public PlainTextDocument(string fileName, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Metnin çıkarılacağı dosyanın adı. |
| loadOptions | LoadOptions | Bir belgeyi yüklerken kullanılacak ek seçenekler.`hükümsüz`. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve bu durum Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Giriş/Çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açmak için bir parola gerekiyor, ancak yanlış bir parola girdiniz. |
| ArgumentException | Dosyanın adı null veya boş dize olamaz. |

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
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve bu durum Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Giriş/Çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açmak için bir parola gerekiyor, ancak yanlış bir parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akarsu, elden çıkarılmış bir nesnedir. |

## Notlar

Belge akışın başlangıcında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler

Akış kullanarak bir Microsoft Word belgesinin içeriğinin düz metin olarak nasıl yükleneceğini gösterir.

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

Bir akıştan düz metin belgesi oluşturur. Şifreleme parolası gibi ek seçeneklerin belirtilmesine olanak tanır.

```csharp
public PlainTextDocument(Stream stream, LoadOptions loadOptions)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Metnin çıkarılacağı akış. |
| loadOptions | LoadOptions | Bir belgeyi yüklerken kullanılacak ek seçenekler.`hükümsüz`. |

### istisnalar

| istisna | şart |
| --- | --- |
| [UnsupportedFileFormatException](../../unsupportedfileformatexception/) | Belge biçimi tanınmıyor veya desteklenmiyor. |
| [FileCorruptedException](../../filecorruptedexception/) | Belge bozuk görünüyor ve yüklenemiyor. |
| Exception | Belgede bir sorun var ve bu durum Aspose.Words geliştiricilerine bildirilmelidir. |
| IOException | Giriş/Çıkış istisnası var. |
| [IncorrectPasswordException](../../incorrectpasswordexception/) | Belge şifrelenmiş ve açmak için bir parola gerekiyor, ancak yanlış bir parola girdiniz. |
| ArgumentNullException | Akış boş olamaz. |
| NotSupportedException | Akış okumayı veya aramayı desteklemiyor. |
| ObjectDisposedException | Akarsu, elden çıkarılmış bir nesnedir. |

## Notlar

Belge akışın başlangıcında saklanmalıdır. Akış rastgele konumlandırmayı desteklemelidir.

## Örnekler

Şifrelenmiş bir Microsoft Word belgesinin içeriğinin akış kullanılarak düz metin olarak nasıl yükleneceğini gösterir.

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
