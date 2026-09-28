---
title: "Метод Aspose::Words::Node::get_Range"
linktitle: "get_Range"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Node::get_Range. Возвращает объект Range, который представляет часть документа, содержащуюся в этом узле, в C++."
type: docs
weight: 12000
url: /ru/cpp/aspose.words/node/get_range/
---
## Node::get_Range method


Возвращает объект [Range](../../range/) , который представляет часть документа, содержащуюся в этом узле.

```cpp
System::SharedPtr<Aspose::Words::Range> Aspose::Words::Node::get_Range()
```


## Примеры



Показывает, как удалить все узлы из диапазона.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Добавьте текст в первый раздел документа, а затем добавьте еще один раздел.
builder->Write(u"Section 1. ");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// Полностью удалите первый раздел, удалив все узлы
// внутри его диапазона, включая сам раздел.
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## См. также

* Class [Range](../../range/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
