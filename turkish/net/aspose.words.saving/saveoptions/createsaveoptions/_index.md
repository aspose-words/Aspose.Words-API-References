---
title: SaveOptions.CreateSaveOptions
second_title: Aspose.Words for .NET API Referansı
description: SaveOptions yöntem. Belirtilen kaydetme biçimine uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(SaveFormat) {#createsaveoptions}

Belirtilen kaydetme biçimine uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveFormat | SaveFormat | Bir kaydetme seçenekleri nesnesinin oluşturulacağı kaydetme biçimi. |

### Geri dönüş değeri

Bir sınıfın nesnesinden türetilen bir nesne[`SaveOptions`](../).

### Örnekler

Büyük belgeleri PDF'ye dönüştürürken bellek tüketimini optimize etme seçeneği gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgenin "Kaydet" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme şeklini değiştirmek için.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Büyük belgelerin kaydetme işlemlerinin bellek kapladığı alanı azaltmak için "MemoryOptimization" özelliğini "true" olarak ayarlayın
// operasyon süresini artırma pahasına.
// Belgeyi normal olarak PDF olarak kaydetmek için "MemoryOptimization" özelliğini "false" olarak ayarlayın.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../saveoptions/)
* toplantı [Aspose.Words](../../../)

---

## CreateSaveOptions(string) {#createsaveoptions_1}

Verilen dosya adında belirtilen dosya uzantısına uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Bu dosya adının uzantısı, oluşturulacak kaydetme seçenekleri nesnesinin sınıfını belirler. |

### Geri dönüş değeri

Bir sınıfın nesnesinden türetilen bir nesne[`SaveOptions`](../).

### Örnekler

Ekli şablonları olmayan belgeler için varsayılan bir şablonun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Otomatik stil güncellemeyi etkinleştir, ancak şablon belgesi ekleme.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Şablon belgesi olmadığından, belgenin stil değişikliklerini izleyecek hiçbir yeri yoktu.
// Bir şablonu otomatik olarak ayarlamak için SaveOptions nesnesini kullanın
// kaydettiğimiz bir belge yoksa.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../saveoptions/)
* toplantı [Aspose.Words](../../../)


