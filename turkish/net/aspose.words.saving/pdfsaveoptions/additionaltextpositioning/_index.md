---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: .NET için Aspose.Words
description: PDF'lerdeki metin konumlandırmasını kontrol etmek için PdfSaveOptions AdditionalTextPositioning özelliğini keşfedin. Belgenizin düzenini zahmetsizce geliştirin!
type: docs
weight: 20
url: /tr/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

Ek metin konumlandırma operatörlerinin yazılıp yazılamayacağını belirten bir bayrak.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## Notlar

Eğer`doğru` , ek metin konumlandırma operatörleri çıktı PDF'sine yazılır. Bu, bazı yazıcılarda yanlış metin konumlandırmasıyla ilgili sorunlarının üstesinden gelmeye yardımcı olabilir. Olumsuz tarafı, artan PDF belge boyutudur.

Varsayılan değer:`YANLIŞ`.

## Örnekler

Ek metin konumlandırma operatörlerinin nasıl yazılacağını gösterin.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // Yanlış metni düzeltmeyi denemek için "AdditionalTextPositioning" özelliğini "true" olarak ayarlayın
    // çıktı PDF'inde, varsa, dosya boyutunun artması pahasına öğe konumlandırması.
    // Belgeyi her zamanki gibi işlemek için "AdditionalTextPositioning" özelliğini "false" olarak ayarlayın.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
