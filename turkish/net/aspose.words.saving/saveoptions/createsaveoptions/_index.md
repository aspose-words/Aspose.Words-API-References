---
title: SaveOptions.CreateSaveOptions
linktitle: CreateSaveOptions
articleTitle: CreateSaveOptions
second_title: .NET için Aspose.Words
description: Tercih ettiğiniz biçime göre özelleştirilmiş kaydetme seçeneklerini kolayca oluşturmak ve belge yönetimi verimliliğinizi artırmak için CreateSaveOptions yöntemini keşfedin.
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

Bir sınıftan türetilen bir nesne[`SaveOptions`](../).

## Örnekler

Büyük belgeleri PDF'ye dönüştürürken bellek tüketimini optimize etmek için bir seçenek gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// Büyük belgelerin kaydetme işlemlerinin bellek ayak izini azaltmak için "MemoryOptimization" özelliğini "true" olarak ayarlayın
// operasyonun süresinin artması pahasına.
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

Belirtilen dosya adında belirtilen dosya uzantısına uygun bir sınıfın kaydetme seçenekleri nesnesini oluşturur.

```csharp
public static SaveOptions CreateSaveOptions(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Bu dosya adının uzantısı, oluşturulacak kaydetme seçenekleri nesnesinin sınıfını belirler. |

### Geri dönüş değeri

Bir sınıftan türetilen bir nesne[`SaveOptions`](../).

## Örnekler

Ekli şablonu olmayan belgeler için varsayılan şablonun nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Otomatik stil güncellemesini etkinleştirin, ancak şablon belge eklemeyin.
doc.AutomaticallyUpdateStyles = true;

Assert.AreEqual(string.Empty, doc.AttachedTemplate);

// Şablon belge olmadığından, belgede stil değişikliklerini izleyecek bir yer yoktu.
// Bir şablonu otomatik olarak ayarlamak için SaveOptions nesnesini kullanın
// eğer kaydettiğimiz bir belgede yoksa.
SaveOptions options = SaveOptions.CreateSaveOptions("Document.DefaultTemplate.docx");
options.DefaultTemplate = MyDir + "Business brochure.dotx";

doc.Save(ArtifactsDir + "Document.DefaultTemplate.docx", options);
```

### Ayrıca bakınız

* class [SaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
