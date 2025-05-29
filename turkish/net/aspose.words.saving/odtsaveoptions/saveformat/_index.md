---
title: OdtSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: OdtSaveOptions SaveFormat özelliğinin, Odt veya Ott formatlarındaki belgeleri kolayca kaydetmenize, uyumluluk ve esneklik sağlamanıza nasıl olanak sağladığını keşfedin.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/odtsaveoptions/saveformat/
---
## OdtSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. Odt veyaOtt .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Örnekler

Kaydedilmiş bir ODT/OTT belgesinin bir parola ile nasıl şifreleneceğini ve ardından Aspose.Words kullanılarak nasıl yükleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Yeni bir OdtSaveOptions oluşturun ve "SaveFormat.Odt" veya "OdtSaveFormat" iletin.
 // veya belgenin kaydedileceği biçim olarak "SaveFormat.Ott".
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Bu belgeyi uygun bir editörle açarsak,
// SaveOptions nesnesinde belirttiğimiz şifreyi bize soracaktır.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Bu belgeyi Aspose.Words kullanarak tekrar açmak veya düzenlemek istersek,
// Yükleme oluşturucusuna doğru parolayı içeren bir LoadOptions nesnesi sağlamamız gerekecek.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
