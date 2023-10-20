---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words for .NET
description: PdfSaveOptions AdditionalTextPositioning mülk. Ek metin konumlandırma operatörlerinin yazıp yazmayacağını belirten bir işaret C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Ek metin konumlandırma operatörlerinin yazıp yazmayacağını belirten bir işaret.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## Notlar

Eğer`doğru` , ek metin konumlandırma operatörleri çıktı PDF'sine yazılır. Bu, bazı yazıcılarda hatalı metin konumlandırmayla ilgili sorunlarının aşılmasına yardımcı olabilir. Dezavantajı ise PDF belge boyutunun artmasıdır.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Ek metin konumlandırma operatörlerinin nasıl yazılacağını gösterin.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Hatalı düzeltmeyi denemek için "AdditionalTextPositioning" özelliğini "true" olarak ayarlayın
    // çıktı PDF'sinde öğe konumlandırma, eğer varsa, dosya boyutunun artması pahasına.
    // Belgeyi her zamanki gibi oluşturmak için "AdditionalTextPositioning" özelliğini "false" olarak ayarlayın.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
