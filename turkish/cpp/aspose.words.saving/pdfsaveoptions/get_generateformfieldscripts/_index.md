---
title: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts yöntemi"
linktitle: "get_GenerateFormFieldScripts"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts yöntemi. PDF'de belirli Microsoft Word form alanı davranışını taklit eden betiklerin oluşturulup oluşturulmayacağını belirtir. C++'ta varsayılan değer false'tur."
type: docs
weight: 18500
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


PDF içinde belirli Microsoft Word form alanı davranışını taklit eden betiklerin üretilip üretilmeyeceğini belirtir. Varsayılan **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## Açıklamalar


Bu seçenek etkinleştirildiğinde, dışa aktarıcı Microsoft Word form alanı davranışını taklit etmek için PDF JavaScript eylemleri oluşturur; örneğin tarih ve saat form alanları biçimlendirme ve doğrulama kurallarıyla.

**true** olarak ayarlandığında, desteklenen davranış PDF JavaScript eylemleri olarak dışa aktarılır. **false** olarak ayarlandığında ise hiçbir form alanı betiği oluşturulmaz.

Betik yürütmesi PDF görüntüleyicisine bağlıdır. Bazı PDF görüntüleyicileri betikleri yok sayabilir, betik yürütmesini kısıtlayabilir veya kullanıcının JavaScript'i etkinleştirmesini isteyebilir.

JavaScript eylemleri PDF/A-1, PDF/A-2 ve PDF/A-3 uyumluluğu tarafından yasaklanmıştır. Bu durumda **false** değeri otomatik olarak kullanılacaktır.
## Ayrıca Bakınız

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
