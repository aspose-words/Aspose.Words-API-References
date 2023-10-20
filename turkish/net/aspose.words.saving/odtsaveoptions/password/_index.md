---
title: OdtSaveOptions.Password
linktitle: Password
articleTitle: Password
second_title: Aspose.Words for .NET
description: OdtSaveOptions Password mülk. Belgeyi şifrelemek için bir parola alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.saving/odtsaveoptions/password/
---
## OdtSaveOptions.Password property

Belgeyi şifrelemek için bir parola alır veya ayarlar.

```csharp
public string Password { get; set; }
```

## Notlar

Belgeyi şifrelemeden kaydetmek için bu özelliğin şu şekilde olması gerekir:`hükümsüz` veya boş dize.

## Örnekler

Kaydedilmiş bir ODT/OTT belgesinin bir parola ile nasıl şifreleneceğini ve ardından Aspose.Words kullanılarak nasıl yükleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Yeni bir OdtSaveOptions oluşturun ve "SaveFormat.Odt"u iletin,
 // veya belgenin kaydedileceği format olarak "SaveFormat.Ott".
OdtSaveOptions saveOptions = new OdtSaveOptions(saveFormat);
saveOptions.Password = "@sposeEncrypted_1145";

string extensionString = FileFormatUtil.SaveFormatToExtension(saveFormat);

// Bu belgeyi uygun bir editörle açarsak,
// SaveOptions nesnesinde belirttiğimiz şifreyi bizden isteyecek.
doc.Save(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString, saveOptions);

FileFormatInfo docInfo = FileFormatUtil.DetectFileFormat(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString);

Assert.IsTrue(docInfo.IsEncrypted);

// Bu belgeyi Aspose.Words kullanarak tekrar açmak veya düzenlemek istersek,
// yükleme yapıcısına doğru parolayı içeren bir LoadOptions nesnesi sağlamamız gerekecek.
doc = new Document(ArtifactsDir + "OdtSaveOptions.Encrypt" + extensionString,
    new LoadOptions("@sposeEncrypted_1145"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [OdtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
