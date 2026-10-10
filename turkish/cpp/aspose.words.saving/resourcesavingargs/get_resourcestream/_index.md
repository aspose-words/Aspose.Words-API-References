---
title: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream metodu"
linktitle: "get_ResourceStream"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream metodu. C++'ta kaynağın kaydedileceği akışı belirtmenizi sağlar."
type: docs
weight: 6000
url: /tr/cpp/aspose.words.saving/resourcesavingargs/get_resourcestream/
---
## ResourceSavingArgs::get_ResourceStream method


Kaynağın kaydedileceği akışı belirtmeye izin verir.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Saving::ResourceSavingArgs::get_ResourceStream() const
```

## Açıklamalar


Bu özellik, kaynakları dosyalar yerine akışlara kaydetmenizi sağlar.

Varsayılan değer **null**'dır. Bu özellik **null** olduğunda, kaynak [ResourceFileName](../get_resourcefilename/) özelliğinde belirtilen bir dosyaya kaydedilir.

[IResourceSavingCallback](../../iresourcesavingcallback/) kullanarak bir kaynağı başka bir kaynakla değiştiremezsiniz. Bu sadece kaynakların kaydedileceği konumun kontrolü için tasarlanmıştır.

## Ayrıca Bakınız

* Class [ResourceSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
