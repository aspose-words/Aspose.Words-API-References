---
title: "Aspose::Words::NodeCollection::Add метод"
linktitle: "Add"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeCollection::Add метод. Добавляет узел в конец коллекции в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/nodecollection/add/
---
## NodeCollection::Add method


Добавляет узел в конец коллекции.

```cpp
void Aspose::Words::NodeCollection::Add(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| узел | const System::SharedPtr\<Aspose::Words::Node\>\& | Узел, который будет добавлен в конец коллекции. |
## Примечания


Узел вставляется как дочерний элемент в объект узла, из которого была создана коллекция.

Если вставляемый узел был создан из другого документа, следует использовать [ImportNode()](../) для импорта узла в текущий документ. Импортированный узел затем можно вставить в текущий документ.

## Примеры



Показывает, как подготовить новый узел раздела для редактирования.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Пустой документ содержит раздел, у которого есть тело, которое, в свою очередь, имеет абзац.
// Мы можем добавить содержимое в этот документ, добавляя такие элементы, как текстовые фрагменты, фигуры или таблицы, в этот абзац.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Если мы добавим новый раздел таким образом, у него не будет тела или каких-либо других дочерних узлов.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Выполните метод "EnsureMinimum", чтобы добавить тело и абзац в этот раздел и начать его редактирование.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## См. также

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
