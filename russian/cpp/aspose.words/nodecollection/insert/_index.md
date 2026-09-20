---
title: "Метод Aspose::Words::NodeCollection::Insert"
linktitle: "Insert"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::NodeCollection::Insert. Вставляет узел в коллекцию по указанному индексу в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words/nodecollection/insert/
---
## NodeCollection::Insert method


Вставляет узел в коллекцию по указанному индексу.

```cpp
void Aspose::Words::NodeCollection::Insert(int32_t index, const System::SharedPtr<Aspose::Words::Node> &node)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| index | int32_t | Нулевой индекс узла. Допускаются отрицательные индексы, указывающие доступ с конца списка. Например, -1 означает последний узел, -2 — предпоследний и т.д. |
| узел | const System::SharedPtr\<Aspose::Words::Node\>\& | Узел для вставки. |
## Примечания


Узел вставляется как дочерний элемент в объект узла, из которого была создана коллекция.

Если индекс равен или больше значения [Count](../get_count/), узел добавляется в конец коллекции.

Если индекс отрицательный и его абсолютное значение больше, чем [Count](../get_count/), узел добавляется в конец коллекции.

Если вставляемый узел был создан из другого документа, следует использовать [ImportNode()](../) для импорта узла в текущий документ. Импортированный узел затем можно вставить в текущий документ.

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
