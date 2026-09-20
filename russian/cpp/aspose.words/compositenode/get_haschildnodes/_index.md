---
title: "метод Aspose::Words::CompositeNode::get_HasChildNodes"
linktitle: "get_HasChildNodes"
second_title: "Справочник API Aspose.Words для C++"
description: "метод Aspose::Words::CompositeNode::get_HasChildNodes. Возвращает true, если у этого узла есть дочерние узлы, в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words/compositenode/get_haschildnodes/
---
## CompositeNode::get_HasChildNodes method


Возвращает **true**, если у этого узла есть дочерние узлы.

```cpp
bool Aspose::Words::CompositeNode::get_HasChildNodes()
```


## Примеры



Показывает, как объединить строки из двух таблиц в одну.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

// Ниже представлены два способа получения таблицы из документа.
// 1 -  Из коллекции "Tables" узла Body:
System::SharedPtr<Aspose::Words::Tables::Table> firstTable = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// 2 -  С использованием метода "GetChild":
auto secondTable = System::ExplicitCast<Aspose::Words::Tables::Table>(doc->GetChild(Aspose::Words::NodeType::Table, 1, true));

// Добавьте все строки из текущей таблицы к следующей.
while (secondTable->get_HasChildNodes())
{
    firstTable->get_Rows()->Add(secondTable->get_FirstRow());
}

// Удалите пустой контейнер таблицы.
secondTable->Remove();

doc->Save(get_ArtifactsDir() + u"Table.CombineTables.docx");
```

## См. также

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
