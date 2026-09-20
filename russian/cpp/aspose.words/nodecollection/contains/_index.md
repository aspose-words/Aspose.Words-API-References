---
title: "Aspose::Words::NodeCollection::Contains метод"
linktitle: "Contains"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeCollection::Contains метод. Определяет, находится ли узел в коллекции в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/nodecollection/contains/
---
## NodeCollection::Contains method


Определяет, находится ли узел в коллекции.

```cpp
bool Aspose::Words::NodeCollection::Contains(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| узел | const System::SharedPtr\<Aspose::Words::Node\>\& | Узел для поиска. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.
## Примечания


Этот метод выполняет линейный поиск; поэтому среднее время выполнения пропорционально [Count](../get_count/).

## Примеры



Показывает, как работать с [NodeCollection](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте текст в документ, вставляя Run'ы с помощью DocumentBuilder.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// Каждый вызов метода "Write" создает новый Run,
// который затем появляется в RunCollection родительского Paragraph.
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// Мы также можем вручную вставить узел в RunCollection.
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// Получайте отдельные run'ы и удаляйте их, чтобы удалить их текст из документа.
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## См. также

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
