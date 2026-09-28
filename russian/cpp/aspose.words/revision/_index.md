---
title: "Класс Aspose::Words::Revision"
linktitle: "Ревизия"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Revision. Представляет ревизию (отслеживаемое изменение) в узле документа или стиле. Используйте RevisionType, чтобы проверить тип этой ревизии. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 52000
url: /ru/cpp/aspose.words/revision/
---
## Revision class


Представляет ревизию (отслеживаемое изменение) в узле документа или стиле. Используйте [RevisionType](./get_revisiontype/), чтобы проверить тип этой ревизии. Чтобы узнать больше, посетите статью документации [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/).

```cpp
class Revision : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Accept](./accept/)() | Принимает эту ревизию. |
| [get_Author](./get_author/)() | Получает или задает автора этой ревизии. Не может быть пустой строкой или **null**. |
| [get_DateTime](./get_datetime/)() | Получает или задает дату/время этой ревизии. |
| [get_Group](./get_group/)() | Получает группу ревизии. Возвращает **null**, если ревизия не принадлежит ни одной группе. |
| [get_ParentNode](./get_parentnode/)() | Получает непосредственный родительский узел (владельца) этой ревизии. Это свойство будет работать для любого типа ревизии, кроме [StyleDefinitionChange](../revisiontype/). |
| [get_ParentStyle](./get_parentstyle/)() | Получает непосредственный родительский стиль (владельца) этой ревизии. Это свойство будет работать только для типа ревизии [StyleDefinitionChange](../revisiontype/). |
| [get_RevisionType](./get_revisiontype/)() const | Получает тип этой ревизии. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Reject](./reject/)() | Отклонить эту ревизию. |
| [set_Author](./set_author/)(const System::String\&) | Сеттер для [Aspose::Words::Revision::get_Author](./get_author/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Сеттер для [Aspose::Words::Revision::get_DateTime](./get_datetime/). |
| static [Type](./type/)() |  |

## Примеры



Показывает, как работать с исправлениями в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Обычное редактирование документа не считается исправлением.
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// Чтобы зарегистрировать наши правки как исправления, необходимо указать автора и затем начать их отслеживание.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// Этот флаг соответствует параметру "Review" -> "Tracking" -> "Track Changes" в Microsoft Word.
// Метод "StartTrackRevisions" не влияет на его значение,
// и документ программно отслеживает исправления, несмотря на то, что значение равно "false".
// Если открыть этот документ в Microsoft Word, он не будет отслеживать исправления.
ASSERT_FALSE(doc->get_TrackRevisions());

// Мы добавили текст с помощью Document Builder, поэтому первое исправление — исправление типа вставки.
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// Удалите run, чтобы создать исправление типа удаления.
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// Добавление нового исправления помещает его в начало коллекции исправлений.
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// Вставленные исправления отображаются в теле документа ещё до того, как мы примем/отклоним исправление.
// Отклонение исправления удалит его узлы из тела. Напротив, узлы, составляющие исправления удаления
// также остаются в документе, пока мы не примем исправление.
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// Принятие исправления удаления удалит его родительский узел из текста абзаца
// и затем удалит само исправление из коллекции.
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// Теперь переместите узел, чтобы создать исправление типа перемещения.
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// Исправление перемещения теперь находится на индексе 1. Отклоните исправление, чтобы удалить его содержимое.
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
