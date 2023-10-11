---
title: PdfSaveOptions.DisplayDocTitle
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Pencerenin başlık çubuğunun belge bilgileri sözlüğünün Başlık girişinden alınan belge başlığını görüntüleyip görüntülemeyeceğini belirten bir işaret.
type: docs
weight: 80
url: /tr/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Pencerenin başlık çubuğunun, belge bilgileri sözlüğünün Başlık girişinden alınan belge başlığını görüntüleyip görüntülemeyeceğini belirten bir işaret.

```csharp
public bool DisplayDocTitle { get; set; }
```

### Notlar

Eğer`YANLIŞ`başlık çubuğunda bunun yerine belgeyi içeren PDF dosyasının adı görüntülenmelidir.

Bu işaret, PDF/UA uyumluluğu için gereklidir.`doğru` x000d_ PDF/UA'ya kaydedilirken değer otomatik olarak kullanılacaktır.

Varsayılan değer:`YANLIŞ`.

### Örnekler

Belgenin başlığının başlık çubuğu olarak nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
// Adobe Acrobat Pro gibi bazı PDF okuyucuları almak için "DisplayDocTitle"ı "true" olarak ayarlayın,
// belgenin "Başlık" yerleşik özelliğinin değerini bu belgeye ait olan sekmede görüntülemek için.
// Bu tür okuyucuların belgenin dosya adını görüntülemesini sağlamak için "DisplayDocTitle"ı "false" olarak ayarlayın.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


