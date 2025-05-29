---
title: OdtSaveOptions
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: .NET için Aspose.Words
description: ODT formatında belgeleri zahmetsizce kaydetmek için OdtSaveOptions oluşturucusunu keşfedin. Bu güçlü araçla iş akışınızı kolaylaştırın!
type: docs
weight: 10
url: /tr/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Odt biçim.

```csharp
public OdtSaveOptions()
```

## Örnekler

Kaydedilmiş bir belgenin eski bir ODT şemasına uygun hale getirilmesinin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Ayrıca bakınız

* class [OdtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## OdtSaveOptions(*string*) {#constructor_2}

Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Odt format şifreyle şifrelenmiş.

```csharp
public OdtSaveOptions(string password)
```

### Ayrıca bakınız

* class [OdtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## OdtSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Odt veya Ott biçim.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveFormat | SaveFormat | OlabilirOdt veyaOtt. |

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
