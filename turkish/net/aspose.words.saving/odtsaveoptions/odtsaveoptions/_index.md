---
title: OdtSaveOptions.OdtSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: OdtSaveOptions inşaatçı. Bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Odt format.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/odtsaveoptions/odtsaveoptions/
---
## OdtSaveOptions() {#constructor}

Bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Odt format.

```csharp
public OdtSaveOptions()
```

### Örnekler

Kaydedilen bir belgenin eski bir ODT şemasına nasıl uygun hale getirileceğini gösterir.

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
* ad alanı [Aspose.Words.Saving](../../odtsaveoptions/)
* toplantı [Aspose.Words](../../../)

---

## OdtSaveOptions(string) {#constructor_2}

Bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Odt format bir şifreyle şifrelendi.

```csharp
public OdtSaveOptions(string password)
```

### Ayrıca bakınız

* class [OdtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../odtsaveoptions/)
* toplantı [Aspose.Words](../../../)

---

## OdtSaveOptions(SaveFormat) {#constructor_1}

Bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Odt veya Ott format.

```csharp
public OdtSaveOptions(SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveFormat | SaveFormat | OlabilirOdt veyaOtt. |

### Örnekler

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OdtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../odtsaveoptions/)
* toplantı [Aspose.Words](../../../)


