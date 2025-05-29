---
title: OoxmlSaveOptions
linktitle: OoxmlSaveOptions
articleTitle: OoxmlSaveOptions
second_title: .NET için Aspose.Words
description: Belgeleri Docx formatında zahmetsizce kaydetmek için OoxmlSaveOptions oluşturucusunu keşfedin. Sorunsuz belge yönetiminin ve gelişmiş uyumluluğun kilidini açın.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/ooxmlsaveoptions/ooxmlsaveoptions/
---
## OoxmlSaveOptions() {#constructor}

Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Docx biçim.

```csharp
public OoxmlSaveOptions()
```

## Örnekler

Kaydedilen bir belgenin uyması gereken OOXML uyumluluk spesifikasyonunun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Uyumluluk seçeneklerini Microsoft Word 2003 ile uyumlu olacak şekilde yapılandırırsak,
// Bir resim eklemek, VML kullanılarak şeklinin tanımlanmasını sağlayacaktır.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);
builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Vml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);

// "ISO/IEC 29500:2008" OOXML standardı VML şekillerini desteklemez.
// SaveOptions nesnesinin "Compliance" özelliğini "OoxmlCompliance.Iso29500_2008_Strict" olarak ayarlarsak,
 // Bu nesneyi geçirirken kaydettiğimiz her belgenin o standarda uyması gerekecektir.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions
{
    Compliance = OoxmlCompliance.Iso29500_2008_Strict,
    SaveFormat = SaveFormat.Docx
};

doc.Save(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx", saveOptions);

// Kaydedilen belgemiz, "ISO/IEC 29500:2008" OOXML standardına uymak için şekli DML kullanarak tanımlar.
doc = new Document(ArtifactsDir + "OoxmlSaveOptions.Iso29500Strict.docx");

Assert.AreEqual(ShapeMarkupLanguage.Dml, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).MarkupLanguage);
```

### Ayrıca bakınız

* class [OoxmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## OoxmlSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#constructor_1}

Bu sınıfın, bir belgeyi kaydetmek için kullanılabilecek yeni bir örneğini başlatır.Docx , Docm ,Dotx ,Dotm veya FlatOpc biçim.

```csharp
public OoxmlSaveOptions(SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveFormat | SaveFormat | OlabilirDocx ,Docm , Dotx ,Dotm veyaFlatOpc . |

## Örnekler

.docx'e dönüştürürken eski kontrol karakterlerinin nasıl destekleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Legacy control character.doc");

// Belgeyi OOXML biçiminde kaydettiğimizde, bir OoxmlSaveOptions nesnesi oluşturabiliriz
// ve ardından belgenin nasıl kaydedileceğini değiştirmek için bunu belgenin kaydetme yöntemine geçiriyoruz.
// "KeepLegacyControlChars" özelliğini korumak için "true" olarak ayarlayın
// Kaydederken "ShortDateTime" eski karakteri.
// "KeepLegacyControlChars" özelliğini kaldırmak için "false" olarak ayarlayın
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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
