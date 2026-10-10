---
title: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages yöntemi"
linktitle: "get_InterpolateImages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages yöntemi. Uyumlu bir okuyucu tarafından görüntü enterpolasyonunun uygulanıp uygulanmayacağını gösteren bir bayrak. **false** belirtildiğinde, bayrak çıktı belgesine yazılmaz ve okuyucunun varsayılan davranışı C++'ta kullanılır."
type: docs
weight: 22000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_interpolateimages/
---
## PdfSaveOptions::get_InterpolateImages method


Uyumlu bir okuyucu tarafından görüntü enterpolasyonunun yapılıp yapılmayacağını gösteren bir bayrak. **false** belirtildiğinde, bayrak çıktı belgesine yazılmaz ve okuyucunun varsayılan davranışı kullanılır.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_InterpolateImages() const
```

## Açıklamalar


Kaynak görüntünün çözünürlüğü çıktı cihazının çözünürlüğünden önemli ölçüde düşük olduğunda, her kaynak örnekleme birçok cihaz pikselini kapsar. Sonuç olarak, görüntüler tırtıklı veya bloklu görünebilir. Bu görsel bozulmalar, renderleme sırasında bir görüntü enterpolasyon algoritması uygulanarak azaltılabilir. Bir kaynak örneklemesi tarafından kapsanan tüm pikseller aynı renk ile boyanmak yerine, görüntü enterpolasyonu komşu örnek değerleri arasında yumuşak bir geçiş üretmeye çalışır.

Uyumlu bir Okuyucu, PDF'nin bu özelliğini uygulamamak ya da istediği herhangi bir enterpolasyon uygulamasını kullanmak isteyebilir.

Varsayılan değer **false**'tur.

Enterpolasyon bayrağı PDF/A uyumluluğu tarafından yasaklanmıştır. PDF/A'ya kaydedilirken **false** değeri otomatik olarak kullanılacaktır.
## Ayrıca Bakınız

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
