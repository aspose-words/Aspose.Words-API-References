---
title: "Aspose::Words::Document::get_VersionsCount yöntemi"
linktitle: "get_VersionsCount"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Document::get_VersionsCount yöntemi. C++'ta DOC belgesinde depolanan belge sürümlerinin sayısını alır."
type: docs
weight: 57000
url: /tr/cpp/aspose.words/document/get_versionscount/
---
## Document::get_VersionsCount method


DOC belgesinde depolanan belge sürümlerinin sayısını alır.

```cpp
int32_t Aspose::Words::Document::get_VersionsCount()
```

## Açıklamalar


Microsoft Word'deki sürümlere Dosya/Sürümler menüsü aracılığıyla erişilir. Microsoft Word yalnızca DOC dosyaları için sürümleri destekler.

Bu özellik, belgenin Aspose.Words'ta açılmadan önce bu belgede belge sürümlerinin depolanıp depolanmadığını algılamayı sağlar. Aspose.Words belge sürümleri için başka bir destek sağlamaz. Bu belgeyi Aspose.Words kullanarak kaydederseniz, belge sürümler olmadan kaydedilir.

## Örnekler



Eski Microsoft Word belgelerinin sürüm sayısı özelliğiyle nasıl çalışılacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Versions.doc");

// Bir belgenin bu özelliğini okuyabiliriz, ancak kaydederken koruyamayız.
ASSERT_EQ(4, doc->get_VersionsCount());

doc->Save(get_ArtifactsDir() + u"Document.VersionsCount.doc");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.VersionsCount.doc");

ASSERT_EQ(0, doc->get_VersionsCount());
```

## Ayrıca Bakınız

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
