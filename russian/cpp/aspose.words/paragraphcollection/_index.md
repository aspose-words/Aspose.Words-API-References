---
title: "Класс Aspose::Words::ParagraphCollection"
linktitle: "ParagraphCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::ParagraphCollection. Предоставляет типизированный доступ к коллекции узлов Paragraph. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 48000
url: /ru/cpp/aspose.words/paragraphcollection/
---
## ParagraphCollection class


Предоставляет типизированный доступ к коллекции узлов [Paragraph](../paragraph/). Чтобы узнать больше, посетите статью документации [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class ParagraphCollection : public Aspose::Words::NodeCollection
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
| [idx_get](./idx_get/)(int32_t) | Получает [Paragraph](../paragraph/) по заданному индексу. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Возвращает нулевой индекс указанного узла. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Вставляет узел в коллекцию по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Удаляет узел из коллекции и из документа. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Удаляет узел по указанному индексу из коллекции и из документа. |
| [ToArray](./toarray/)() | Копирует все абзацы из коллекции в новый массив абзацев. |
| static [Type](./type/)() |  |

## Примеры



Показывает, как проверить, является ли абзац перемещённой правкой.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Этот документ содержит правки «Move», которые появляются, когда мы выделяем текст курсором,
// а затем перетаскиваем его, чтобы переместить в другое место
// во время отслеживания правок в Microsoft Word через «Review» -> «Track changes».
ASSERT_EQ(6, doc->get_Revisions()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Revision>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Revision> r)>>([](System::SharedPtr<Aspose::Words::Revision> r) -> bool
{
    return r->get_RevisionType() == Aspose::Words::RevisionType::Moving;
}))));

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();

// Правки перемещения состоят из пар правок «Move from» и «Move to».
// Эти правки являются потенциальными изменениями документа, которые мы можем принять или отклонить.
// Прежде чем принять/отклонить правку перемещения, документ
// должен отслеживать как исходные, так и конечные места текста.
// Второй и четвёртый абзацы определяют одну такую правку, поэтому оба имеют одинаковое содержание.
ASSERT_EQ(paragraphs->idx_get(1)->GetText(), paragraphs->idx_get(3)->GetText());

// Правка «Move from» — это абзац, из которого мы перетащили текст.
// Если мы примем правку, этот абзац исчезнет,
// а другой останется и больше не будет правкой.
ASSERT_TRUE(paragraphs->idx_get(1)->get_IsMoveFromRevision());

// Правка «Move to» — это абзац, в который мы перетащили текст.
// Если мы отклоним правку, этот абзац исчезнет, а другой останется.
ASSERT_TRUE(paragraphs->idx_get(3)->get_IsMoveToRevision());
```

## См. также

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
