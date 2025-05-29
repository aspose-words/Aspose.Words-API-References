---
title: PdfSaveOptions.UseSdtTagAsFormFieldName
linktitle: UseSdtTagAsFormFieldName
articleTitle: UseSdtTagAsFormFieldName
second_title: .NET için Aspose.Words
description: PdfSaveOptions UseSdtTagAsFormFieldName özelliğinin, daha iyi organizasyon ve netlik için SDT denetim etiketlerini kullanarak PDF formlarını nasıl geliştirdiğini keşfedin.
type: docs
weight: 340
url: /tr/net/aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/
---
## PdfSaveOptions.UseSdtTagAsFormFieldName property

PDF'deki form alanının adı olarak SDT denetim Etiketi veya Kimlik özelliğinin kullanılıp kullanılmayacağını belirtir.

```csharp
public bool UseSdtTagAsFormFieldName { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ`.

Ayarlandığında`YANLIŞ`, SDT kontrolünün Id özelliği PDF'deki form alanının adı olarak kullanılır.

Ayarlandığında`doğru`, SDT denetiminin Etiket özelliği PDF'deki form alanının adı olarak kullanılır.

Eğer ayarlanırsa`doğru` ve Tag boş ise, Id özelliği form alan adı olarak kullanılacaktır.

Eğer ayarlanırsa`doğru` ve Etiket değerleri benzersiz değilse, yinelenen Etiket değerleri build benzersiz PDF form alanı adlarına dönüştürülecektir.

## Örnekler

PDF'de SDT denetiminin Etiket veya Kimlik özelliğinin form alanı adı olarak nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Form fields.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PreserveFormFields = true;
// 'false' olarak ayarlandığında, SDT kontrolünün Id özelliği PDF'deki form alanının adı olarak kullanılır.
// 'true' olarak ayarlandığında, SDT denetiminin Etiket özelliği PDF'deki form alanının adı olarak kullanılır.
saveOptions.UseSdtTagAsFormFieldName = true;

doc.Save(ArtifactsDir + "PdfSaveOptions.SdtTagAsFormFieldName.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
