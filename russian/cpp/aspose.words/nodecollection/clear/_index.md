---
title: "Aspose::Words::NodeCollection::Clear метод"
linktitle: "Clear"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::NodeCollection::Clear метод. Удаляет все узлы из этой коллекции и из документа в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/nodecollection/clear/
---
## NodeCollection::Clear method


Удаляет все узлы из этой коллекции и из документа.

```cpp
void Aspose::Words::NodeCollection::Clear()
```


## Примеры



Показывает, как удалить все разделы из документа.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

// Этот документ имеет один раздел с несколькими дочерними узлами, содержащими и отображающими всё содержимое документа.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(17, doc->get_Sections()->idx_get(0)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(u"Hello World!\r\rHello Word!\r\r\rHello World!", doc->GetText().Trim());

// Очистите коллекцию разделов, что удалит всех дочерних элементов документа.
doc->get_Sections()->Clear();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
ASSERT_EQ(System::String::Empty, doc->GetText().Trim());
```

## См. также

* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
