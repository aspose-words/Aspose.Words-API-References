---
title: "Aspose::Words::RevisionGroup class"
linktitle: "RevisionGroup"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::RevisionGroup class. Представляет группу последовательных объектов Revision. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 54000
url: /ru/cpp/aspose.words/revisiongroup/
---
## RevisionGroup class


Представляет группу последовательных объектов [Revision](../revision/). Чтобы узнать больше, посетите статью документации [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class RevisionGroup : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Author](./get_author/)() | Получает автора этой группы ревизий. |
| [get_RevisionType](./get_revisiontype/)() | Получает тип ревизий, включенных в эту группу. |
| [get_Text](./get_text/)() | Возвращает вставленный/удалённый/перемещённый текст или описание изменения формата. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
