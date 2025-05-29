---
title: PdfSaveOptions.PreserveFormFields
linktitle: PreserveFormFields
articleTitle: PreserveFormFields
second_title: .NET için Aspose.Words
description: PdfSaveOptions' PreserveFormFields özelliğinin PDF'lerdeki Microsoft Word form alanlarını nasıl koruduğunu veya bunları metne nasıl dönüştürdüğünü keşfedin. Belge kalitenizi artırın!
type: docs
weight: 280
url: /tr/net/aspose.words.saving/pdfsaveoptions/preserveformfields/
---
## PdfSaveOptions.PreserveFormFields property

Microsoft Word form alanlarının PDF'de form alanları olarak korunacağını veya metne dönüştürüleceğini belirtir. Varsayılan`YANLIŞ` .

```csharp
public bool PreserveFormFields { get; set; }
```

## Notlar

Microsoft Word form alanları metin girişi, açılır liste ve onay kutusu denetimlerini içerir.

Ayarlandığında`YANLIŞ` , bu alanlar PDF'ye metin olarak aktarılacaktır. olarak ayarlandığında`doğru`, bu alanlar PDF form alanları olarak dışarı aktarılacaktır.

Form alanlarını PDF'ye form alanı olarak aktarırken bazı biçimlendirme kayıpları meydana gelebilir, çünkü PDF form alanları Microsoft Word form alanlarının tüm özelliklerini desteklemez.

Ayrıca çıktı boyutu içerik boyutuna bağlıdır çünkü Microsoft Word'deki düzenlenebilir formlar satır içi nesnelerdir.

PDF/A uyumluluğu nedeniyle düzenlenebilir formlar yasaktır.`YANLIŞ` PDF/A'ya kaydederken değer otomatik olarak kullanılacaktır .

PDF/UA'ya kaydederken form alanları desteklenmiyor.`YANLIŞ` değer otomatik olarak kullanılacaktır.

## Örnekler

Save metodu ve PdfSaveOptions sınıfı kullanılarak bir belgenin PDF formatına nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Please select a fruit: ");

// Kullanıcının bir dizi dize arasından bir seçenek seçmesine izin verecek bir açılır kutu ekleyin.
builder.InsertComboBox("MyComboBox", new[] { "Apple", "Banana", "Cherry" }, 0);

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions pdfOptions = new PdfSaveOptions();

// Çıktı PDF'inde form alanlarını etkileşimli nesneler olarak kaydetmek için "PreserveFormFields" özelliğini "true" olarak ayarlayın.
// Belgedeki tüm form alanlarını dondurmak için "PreserveFormFields" özelliğini "false" olarak ayarlayın
// mevcut değerlerini ve çıktı PDF'inde düz metin olarak görüntüler.
pdfOptions.PreserveFormFields = preserveFormFields;

doc.Save(ArtifactsDir + "PdfSaveOptions.PreserveFormFields.pdf", pdfOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
