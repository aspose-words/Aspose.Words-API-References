---
title: "Aspose::Words::RunCollection class"
linktitle: "RunCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::RunCollection class. Обеспечивает типизированный доступ к коллекции узлов Run. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 57000
url: /ru/cpp/aspose.words/runcollection/
---
## RunCollection class


Обеспечивает типизированный доступ к коллекции узлов [Run](../run/). Чтобы узнать больше, посетите статью документации [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class RunCollection : public Aspose::Words::NodeCollection
```

## Методы

| Метод | Описание |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Добавляет узел в конец коллекции. |
| [Clear](../nodecollection/clear/)() | Удаляет все узлы из этой коллекции и из документа. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Определяет, находится ли узел в коллекции. |
| [get_Count](../nodecollection/get_count/)() | Получает количество узлов в коллекции. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Предоставляет простую итерацию в стиле "foreach" по коллекции узлов. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает [Run](../run/) по заданному индексу. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает нулевой индекс указанного узла. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Вставляет узел в коллекцию по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Удаляет узел по указанному индексу из коллекции и из документа. |
| [ToArray](./toarray/)() | Копирует все узлы run из коллекции в новый массив узлов run. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как определить тип ревизии встроенного узла.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Когда мы редактируем документ при включённой опции "Track Changes", доступной через Review -> Tracking,
// в Microsoft Word, внесённые нами изменения считаются ревизиями.
// При редактировании документа с использованием Aspose.Words мы можем начать отслеживание ревизий, вызвав
// вызывая метод документа "StartTrackRevisions" и прекращая отслеживание с помощью метода "StopTrackRevisions".
// Мы можем либо принять ревизии, чтобы включить их в документ
// либо отклонить их, чтобы эффективно отменить предложенное изменение.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Родительским узлом ревизии является run, к которой относится ревизия. Run — это узел Inline.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Ниже представлены пять типов ревизий, которые могут пометить Inline‑узел.
// 1 -  Вставка "insert" ревизии:
// Эта ревизия происходит, когда мы вставляем текст при отслеживании изменений.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Формат "format" ревизии:
// Эта ревизия происходит, когда мы изменяем форматирование текста при отслеживании изменений.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Ревизия "move from" ревизии:
// Когда мы выделяем текст в Microsoft Word и затем перетаскиваем его в другое место в документе
// при отслеживании изменений появляются две ревизии.
// Ревизия "move from" является копией исходного текста до его перемещения.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Ревизия "move to" ревизии:
// Ревизия "move to" — это текст, который мы переместили в новое положение в документе.
// Ревизии "Move from" и "move to" появляются парами для каждой выполненной нами ревизии перемещения.
// Принятие ревизии перемещения удаляет ревизию "move from" и её текст,
// и сохраняет текст из ревизии "move to".
// Отклонение ревизии перемещения, наоборот, сохраняет ревизию "move from" и удаляет ревизию "move to".
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Ревизия "delete" ревизии:
// Эта ревизия происходит, когда мы удаляем текст при отслеживании изменений. Когда мы удаляем текст таким образом,
// он останется в документе как ревизия, пока мы не примем её,
// что навсегда удалит текст, или отклонит ревизию, что сохранит удалённый текст на месте.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## См. также

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
