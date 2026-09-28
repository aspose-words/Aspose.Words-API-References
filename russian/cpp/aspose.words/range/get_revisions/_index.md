---
title: "Метод Aspose::Words::Range::get_Revisions"
linktitle: "get_Revisions"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Range::get_Revisions. Получает коллекцию правок (отслеживаемых изменений), существующих в этом диапазоне в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/range/get_revisions/
---
## Range::get_Revisions method


Получает коллекцию исправлений (отслеживаемых изменений), существующих в этом диапазоне.

```cpp
System::SharedPtr<Aspose::Words::RevisionCollection> Aspose::Words::Range::get_Revisions()
```

## Примечания


Возвращаемая коллекция является «живой» коллекцией, что означает, что если вы удалите части документа, содержащие исправления, удалённые исправления автоматически исчезнут из этой коллекции.

## Примеры



Показывает, как работать с правками в диапазоне.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
for (auto&& revision : System::IterateOver(paragraph->get_Range()->get_Revisions()))
{
    if (revision->get_RevisionType() == Aspose::Words::RevisionType::Deletion)
    {
        revision->Accept();
    }
}

// Отклоните правки первого раздела.
doc->get_FirstSection()->get_Range()->get_Revisions()->RejectAll();
```

## См. также

* Class [RevisionCollection](../../revisioncollection/)
* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
