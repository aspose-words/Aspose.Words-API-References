---
title: PdfSaveOptions.DisplayDocTitle
linktitle: DisplayDocTitle
articleTitle: DisplayDocTitle
second_title: .NET için Aspose.Words
description: PdfSaveOptions DisplayDocTitle özelliğinin, kolay tanımlama için Windows başlık çubuğunda belge başlıklarını göstererek PDF deneyiminizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 90
url: /tr/net/aspose.words.saving/pdfsaveoptions/displaydoctitle/
---
## PdfSaveOptions.DisplayDocTitle property

Pencerenin başlık çubuğunun, belge bilgi sözlüğünün Başlık girişinden alınan belge başlığını görüntüleyip görüntülemeyeceğini belirten bir bayrak.

```csharp
public bool DisplayDocTitle { get; set; }
```

## Notlar

Eğer`YANLIŞ`, başlık çubuğu bunun yerine belgeyi içeren PDF dosyasının adını görüntülemelidir.

Bu bayrak PDF/UA uyumluluğu için gereklidir.`doğru` saving PDF/UA'ya kaydedildiğinde bu değer otomatik olarak kullanılacaktır.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Belgenin başlığının başlık çubuğunda nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.BuiltInDocumentProperties.Title = "Windows bar pdf title";

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
// Adobe Acrobat Pro gibi bazı PDF okuyucularını almak için "DisplayDocTitle" değerini "true" olarak ayarlayın.
// Bu belgeye ait sekmede belgenin "Başlık" yerleşik özelliğinin değerini görüntülemek için.
// Bu tür okuyucuların belgenin dosya adını görüntülemesini sağlamak için "DisplayDocTitle" değerini "false" olarak ayarlayın.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { DisplayDocTitle = displayDocTitle };

doc.Save(ArtifactsDir + "PdfSaveOptions.DocTitle.pdf", pdfSaveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
