---
title: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields yöntemi"
linktitle: "get_PreserveFormFields"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields yöntemi. Microsoft Word form alanlarını PDF içinde form alanı olarak koruyup korumayacağını veya metne dönüştürülüp dönüştürüleceğini belirtir. Varsayılan değer C++'da false'dur."
type: docs
weight: 28000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_preserveformfields/
---
## PdfSaveOptions::get_PreserveFormFields method


Microsoft Word form alanlarını PDF'de form alanı olarak koruyup korumayacağını veya metne dönüştürülüp dönüştürülmeyeceğini belirtir. Varsayılan **false** değeridir.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_PreserveFormFields() const
```

## Açıklamalar


Microsoft Word form alanları metin girişi, açılır menü ve onay kutusu denetimlerini içerir.

**false** olarak ayarlandığında, bu alanlar PDF'ye metin olarak dışa aktarılır. **true** olarak ayarlandığında, bu alanlar PDF form alanları olarak dışa aktarılır.

Form alanlarını PDF'ye form alanı olarak dışa aktarırken, PDF form alanları Microsoft Word form alanlarının tüm özelliklerini desteklemediği için bazı biçimlendirme kayıpları meydana gelebilir.

Ayrıca, çıktı boyutu içeriğin boyutuna bağlıdır çünkü Microsoft Word'deki düzenlenebilir formlar satır içi nesnelerdir.
## Ayrıca Bakınız

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
