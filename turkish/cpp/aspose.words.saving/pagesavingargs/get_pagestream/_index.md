---
title: "Aspose::Words::Saving::PageSavingArgs::get_PageStream yöntemi"
linktitle: "get_PageStream"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::PageSavingArgs::get_PageStream yöntemi. Belge sayfasının C++'ta kaydedileceği akışı belirtmeye olanak tanır."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/pagesavingargs/get_pagestream/
---
## PageSavingArgs::get_PageStream method


Belge sayfasının kaydedileceği akışı belirtmeye izin verir.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::PageSavingArgs::get_PageStream() const
```

## Açıklamalar


Bu özellik, belge sayfalarını dosyalar yerine akışlara kaydetmenizi sağlar.

Varsayılan değer **null**'dır. Bu özellik **null** olduğunda, belge sayfası [PageFileName](../get_pagefilename/) özelliğinde belirtilen bir dosyaya kaydedilir.

Hem [PageStream](./) hem de [PageFileName](../get_pagefilename/) ayarlanmışsa, PageStream kullanılacaktır.

## Ayrıca Bakınız

* Class [PageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
