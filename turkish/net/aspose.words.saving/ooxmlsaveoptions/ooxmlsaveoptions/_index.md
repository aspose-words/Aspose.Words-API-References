---
title: OoxmlSaveOptions.OoxmlSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: OoxmlSaveOptions inşaatçı. Dosyaya bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Docx biçim.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions() {#constructor}

Dosyaya bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Docx biçim.

```csharp
public OoxmlSaveOptions()
```

### Örnekler

Kaydedilmiş bir belgenin uyulması için bir OOXML uyumluluk özelliğinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Uyumluluk seçeneklerini Microsoft Word 2003 ile uyumlu olacak şekilde yapılandırırsak,
// bir resim eklemek, şeklini VML kullanarak tanımlayacaktır.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// "ISO/IEC 29500:2008" OOXML standardı VML şekillerini desteklemez.
// SaveOptions nesnesinin "Compliance" özelliğini "OoxmlCompliance.Iso29500_2008_Strict" olarak ayarlarsak,
 // bu nesneyi geçerken kaydettiğimiz herhangi bir belgenin bu standarda uyması gerekecek.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Kayıtlı belgemiz, "ISO/IEC 29500:2008" OOXML standardına uymak için DML kullanarak şekli tanımlar.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Ayrıca bakınız

* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* toplantı [Aspose.Words](../../../)

---

## OoxmlSaveOptions(SaveFormat) {#constructor_1}

Dosyaya bir belgeyi kaydetmek için kullanılabilecek bu sınıfın yeni bir örneğini başlatır.Docx , Docm ,Dotx ,Dotm or FlatOpc biçim.

```csharp
public OoxmlSaveOptions(SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveFormat | SaveFormat | OlabilirDocx ,Docm , Dotx ,Dotm veyaFlatOpc . |

### Örnekler

.docx'e dönüştürürken eski kontrol karakterlerinin nasıl destekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Belgeyi OOXML formatında kaydettiğimizde bir OoxmlSaveOptions nesnesi oluşturabiliriz.
// ve ardından belgeyi kaydetme şeklimizi değiştirmek için belgenin kaydetme yöntemine iletin.
// Korumak için "KeepLegacyControlChars" özelliğini "true" olarak ayarlayın
// kaydederken "ShortDateTime" eski karakteri.
// Kaldırmak için "KeepLegacyControlChars" özelliğini "false" olarak ayarlayın
// çıktı belgesindeki "ShortDateTime" eski karakteri.
OoxmlSaveOptions so = new OoxmlSaveOptions(SaveFormat.Docx);
so.KeepLegacyControlChars = keepLegacyControlChars;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx", so);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.KeepLegacyControlChars.docx");

Assert.AreEqual(keepLegacyControlChars ? "\u0013date \\@ \"MM/dd/yyyy\"\u0014\u0015\f" : "\u001e\f",
    doc.FirstSection.Body.GetText());
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../ooxmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


