---
title: "Aspose::Words::RevisionGroup::get_RevisionType метод"
linktitle: "get_RevisionType"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::RevisionGroup::get_RevisionType метод. Получает тип правок, включенных в эту группу, в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/revisiongroup/get_revisiontype/
---
## RevisionGroup::get_RevisionType method


Получает тип ревизий, включенных в эту группу.

```cpp
Aspose::Words::RevisionType Aspose::Words::RevisionGroup::get_RevisionType()
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

* Enum [RevisionType](../../revisiontype/)
* Class [RevisionGroup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
