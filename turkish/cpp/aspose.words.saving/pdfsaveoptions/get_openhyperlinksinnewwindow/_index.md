---
title: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow yöntemi"
linktitle: "get_OpenHyperlinksInNewWindow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow yöntemi. Çıktı PDF belgesindeki hiperlinklerin bir tarayıcıda yeni bir pencere (veya sekme) içinde açılmaya zorlanıp zorlanmayacağını belirleyen bir değeri alır veya ayarlar C++'da."
type: docs
weight: 24000
url: /tr/cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


Çıktı Pdf belgesindeki köprülerin yeni bir pencere (veya sekme) içinde açılmaya zorlanıp zorlanmayacağını belirleyen bir değeri alır veya ayarlar.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## Açıklamalar


Varsayılan değer **false**'dır. Bu değer **true** olarak ayarlandığında, köprüler JavaScript kodu kullanılarak kaydedilir. JavaScript kodu **app.launchURL("URL", true);** şeklindedir, burada **URL** bir köprüdür.

Bu seçeneğin **true** olarak ayarlandığında, köprülerin bazı PDF okuyucularında (ör. Chrome, Firefox) çalışmayabileceğini unutmayın.

JavaScript eylemleri PDF/A-1, PDF/A-2 ve PDF/A-3 uyumluluğu tarafından yasaklanmıştır. Bu durumda **false** değeri otomatik olarak kullanılacaktır.
## Ayrıca Bakınız

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
