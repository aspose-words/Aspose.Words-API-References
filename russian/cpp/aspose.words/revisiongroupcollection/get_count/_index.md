---
title: "Aspose::Words::RevisionGroupCollection::get_Count метод"
linktitle: "get_Count"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::RevisionGroupCollection::get_Count метод. Возвращает количество групп исправлений в коллекции в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/revisiongroupcollection/get_count/
---
## RevisionGroupCollection::get_Count method


Возвращает количество групп правок в коллекции.

```cpp
int32_t Aspose::Words::RevisionGroupCollection::get_Count()
```


## Примеры



Показывает, как вывести информацию о группе ревизий в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

ASSERT_EQ(7, doc->get_Revisions()->get_Groups()->get_Count());

for (auto&& group : doc->get_Revisions()->get_Groups())
{
    std::cout << System::String::Format(u"Revision author: {0}; Revision type: {1} \n\tRevision text: {2}", group->get_Author(), group->get_RevisionType(), group->get_Text()) << std::endl;
}
```

## См. также

* Class [RevisionGroupCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
