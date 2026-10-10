---
title: "Aspose::Words::RevisionGroupCollection::idx_get metodu"
linktitle: "idx_get"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::RevisionGroupCollection::idx_get metodu. C++'ta belirtilen indeksteki revizyon grubunu döndürür."
type: docs
weight: 9000
url: /tr/cpp/aspose.words/revisiongroupcollection/idx_get/
---
## RevisionGroupCollection::idx_get method


Belirtilen indeksteki bir revizyon grubunu döndürür.

```cpp
System::SharedPtr<Aspose::Words::RevisionGroup> Aspose::Words::RevisionGroupCollection::idx_get(int32_t index)
```


## Örnekler



Bir belgede revizyon grubunun nasıl alınacağını gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## Ayrıca Bakınız

* Class [RevisionGroup](../../revisiongroup/)
* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
