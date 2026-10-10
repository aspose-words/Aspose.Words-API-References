---
title: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName metodu"
linktitle: "get_UseSdtTagAsFormFieldName"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName metodu. PDF içinde form alanı adı olarak SDT kontrol Tag veya Id özelliğinin kullanılacağını belirtir (C++)."
type: docs
weight: 32500
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_usesdttagasformfieldname/
---
## PdfSaveOptions::get_UseSdtTagAsFormFieldName method


PDF'de form alanı adı olarak SDT kontrol Etiketi (Tag) mi yoksa Id özelliği mi kullanılacağını belirtir.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_UseSdtTagAsFormFieldName() const
```

## Açıklamalar


Varsayılan değer **false**'tur.

**false** olarak ayarlandığında, SDT kontrol Id özelliği PDF içinde form alanı adı olarak kullanılır.

**true** olarak ayarlandığında, SDT kontrol Tag özelliği PDF içinde form alanı adı olarak kullanılır.

**true** olarak ayarlandığında ve Tag boş ise, Id özelliği form alanı adı olarak kullanılacaktır.

**true** olarak ayarlandığında ve Tag değerleri benzersiz değilse, yinelenen Tag değerleri benzersiz PDF form alanı adları oluşturmak için değiştirilecektir.
## Ayrıca Bakınız

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
