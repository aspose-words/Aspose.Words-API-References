---
title: "Aspose::Words::RevisionGroup::get_Text метод"
linktitle: "get_Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::RevisionGroup::get_Text метод. Возвращает вставленный/удалённый/перемещённый текст или описание изменения формата в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/revisiongroup/get_text/
---
## RevisionGroup::get_Text method


Возвращает вставленный/удалённый/перемещённый текст или описание изменения формата.

```cpp
System::String Aspose::Words::RevisionGroup::get_Text()
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

* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
