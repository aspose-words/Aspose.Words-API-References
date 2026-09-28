---
title: "Aspose::Words::CompositeNode::get_LastChild метод"
linktitle: "get_LastChild"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::CompositeNode::get_LastChild метод. Получает последний дочерний узел данного узла в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/compositenode/get_lastchild/
---
## CompositeNode::get_LastChild method


Возвращает последнего дочернего узла.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_LastChild() const
```


## Примеры



Показывает, как использовать методы [Node](../../node/) и [CompositeNode](../) для удаления раздела перед последним разделом в документе.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// Оба раздела являются соседями друг друга.
auto lastSection = System::ExplicitCast<Aspose::Words::Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Aspose::Words::Section>(lastSection->get_PreviousSibling());

// Удалите раздел, основываясь на его соседних отношениях с другим разделом.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild<System::SharedPtr<Aspose::Words::Section>>(firstSection);
}

// Раздел, который мы удалили, был первым, оставив документ только со вторым.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## См. также

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
