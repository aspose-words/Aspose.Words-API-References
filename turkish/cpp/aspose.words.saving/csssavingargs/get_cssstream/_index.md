---
title: "Aspose::Words::Saving::CssSavingArgs::get_CssStream yöntemi"
linktitle: "get_CssStream"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::CssSavingArgs::get_CssStream yöntemi. CSS bilgisinin C++'ta kaydedileceği akışı belirtmenizi sağlar."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.saving/csssavingargs/get_cssstream/
---
## CssSavingArgs::get_CssStream method


CSS bilgisinin kaydedileceği akışı belirtmeye izin verir.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::CssSavingArgs::get_CssStream() const
```

## Açıklamalar


Bu özellik, CSS bilgisini bir akışa kaydetmenizi sağlar.

Varsayılan değer **null**'dır. Bu özellik, CSS bilgisinin bir dosyaya kaydedilmesini veya HTML belgesine gömülmesini engellemez. CSS dışa aktarmayı engellemek için [IsExportNeeded](../get_isexportneeded/) özelliğini kullanın.

[ICssSavingCallback](../../icsssavingcallback/) kullanarak CSS'i başka bir şeyle değiştiremezsiniz. Bu yalnızca CSS'i bir akışa kaydetmek için tasarlanmıştır.

## Ayrıca Bakınız

* Class [CssSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
