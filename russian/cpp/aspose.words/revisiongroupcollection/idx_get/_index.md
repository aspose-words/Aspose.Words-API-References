---
title: "Метод idx_get класса Aspose::Words::RevisionGroupCollection"
linktitle: "idx_get"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод idx_get класса Aspose::Words::RevisionGroupCollection. Возвращает группу правок по указанному индексу в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words/revisiongroupcollection/idx_get/
---
## RevisionGroupCollection::idx_get method


Возвращает группу правок по указанному индексу.

```cpp
System::SharedPtr<Aspose::Words::RevisionGroup> Aspose::Words::RevisionGroupCollection::idx_get(int32_t index)
```


## Примеры



Показывает, как получить группу правок в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::RevisionGroup> revisionGroup = doc->get_Revisions()->get_Groups()->idx_get(0);
```

## См. также

* Class [RevisionGroup](../../revisiongroup/)
* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
