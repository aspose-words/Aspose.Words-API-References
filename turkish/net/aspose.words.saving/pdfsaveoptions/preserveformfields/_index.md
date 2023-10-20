---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: Aspose.Words for .NET
description: PdfSaveOptions PreserveFormFields mülk. Microsoft Word form alanlarının PDFdeki form alanları olarak mı korunacağını yoksa metne mi dönüştürüleceğini belirtir. VarsayılanYANLIŞ  C#'da.
type: docs
weight: 270
url: /tr/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Microsoft Word form alanlarının PDF'deki form alanları olarak mı korunacağını yoksa metne mi dönüştürüleceğini belirtir. Varsayılan:`YANLIŞ` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Notlar

Microsoft Word form alanları metin girişi, açılır menü ve onay kutusu kontrollerini içerir.

olarak ayarlandığında`YANLIŞ` , bu alanlar metin olarak PDF'ye aktarılacaktır. olarak ayarlandığında`doğru`, bu alanlar PDF form alanları olarak dışa aktarılacaktır.

Form alanlarını PDF'ye form alanları olarak dışa aktarırken, PDF form alanları Microsoft Word form alanlarının tüm özelliklerini desteklemediğinden bazı biçimlendirme kayıpları meydana gelebilir.

Ayrıca, Microsoft Word'deki düzenlenebilir formlar satır içi nesneler olduğundan, çıktı boyutu içerik boyutuna bağlıdır.

Düzenlenebilir formlar PDF/A uyumluluğu nedeniyle yasaktır.`YANLIŞ` PDF/A'ya kaydederken otomatik olarak değeri kullanılacaktır.

PDF/UA'ya kaydederken form alanları desteklenmez.`YANLIŞ` değer otomatik olarak kullanılacaktır.

## Örnekler

Kaydet yöntemini ve PdfSaveOptions sınıfını kullanarak bir belgenin PDF biçiminde nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Kullanıcının bir dizi dizeden bir seçenek seçmesine olanak tanıyacak bir açılan kutu ekleyin.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Form alanlarını çıktı PDF'sinde etkileşimli nesneler olarak kaydetmek için "PreserveFormFields" özelliğini "true" olarak ayarlayın.
// Belgedeki tüm form alanlarını dondurmak için "PreserveFormFields" özelliğini "false" olarak ayarlayın
// mevcut değerleri ve bunları çıktı PDF'sinde düz metin olarak görüntüleyin.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
