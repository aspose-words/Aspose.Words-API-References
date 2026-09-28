---
title: "Метод Aspose::Words::Node::get_PreviousSibling"
linktitle: "get_PreviousSibling"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Node::get_PreviousSibling. Получает узел, непосредственно предшествующий этому узлу в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


Возвращает узел, непосредственно предшествующий этому узлу.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## Примеры



Показывает, как использовать методы [Node](../) и [CompositeNode](../../compositenode/) для удаления раздела перед последним разделом в документе.
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

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
