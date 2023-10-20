---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
articleTitle: CreateSaveOptions
second_title: Aspose.Words for .NET
description: SaveOptions CreateSaveOptions yöntem. Belirtilen kaydetme biçimine uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/saveoptions/createsaveoptions/
---
## CreateSaveOptions(*[SaveFormat](../../../aspose.words/saveformat/)*) {#createsaveoptions}

Belirtilen kaydetme biçimine uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur.

```csharp
public static SaveOptions CreateSaveOptions(SaveFormat saveFormat)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| saveFormat | SaveFormat | Kaydetme seçenekleri nesnesinin oluşturulacağı kaydetme biçimi. |

### Geri dönüş değeri

Türetilen bir sınıfın nesnesi[`SaveOptions`](../).

## Örnekler

Büyük belgeleri PDF'ye dönüştürürken bellek tüketimini optimize etme seçeneğini gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Büyük belgelerin kaydetme işlemlerinin bellek alanını azaltmak için "MemoryOptimization" özelliğini "true" olarak ayarlayın
// operasyonun süresini arttırma pahasına.
// Belgeyi normal şekilde PDF olarak kaydetmek için "MemoryOptimization" özelliğini "false" olarak ayarlayın.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### Ayrıca bakınız

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)

---

## CreateSaveOptions(*string*) {#createsaveoptions_1}

Verilen dosya adında belirtilen dosya uzantısına uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Bu dosya adının uzantısı, oluşturulacak kaydetme seçenekleri nesnesinin sınıfını belirler. |

### Geri dönüş değeri

Türetilen bir sınıfın nesnesi[`SaveOptions`](../).

## Örnekler

Ekli şablonları olmayan belgeler için varsayılan şablonun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Otomatik stil güncellemeyi etkinleştirin ancak şablon belgesi eklemeyin.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Şablon belge olmadığından belgenin stil değişikliklerini izleyecek yeri yoktu.
// Şablonu otomatik olarak ayarlamak için SaveOptions nesnesini kullanın
// eğer kaydettiğimiz belgede belge yoksa.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
