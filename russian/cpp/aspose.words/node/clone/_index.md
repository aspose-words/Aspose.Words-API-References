---
title: "Метод Aspose::Words::Node::Clone"
linktitle: "Клонировать"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Node::Clone. Создает дубликат узла в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/node/clone/
---
## Node::Clone method


Создаёт дубликат узла.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::Clone(bool isCloneChildren)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| isCloneChildren | bool | True, чтобы рекурсивно клонировать поддерево под указанным узлом; false, чтобы клонировать только сам узел. |

### ReturnValue

Клонированный узел.
## Примечания


Этот метод служит конструктором копирования для узлов. Клонированный узел не имеет родителя, но принадлежит тому же документу, что и оригинальный узел.

Этот метод всегда выполняет глубокое копирование узла. Параметр *isCloneChildren* указывает, следует ли также копировать все дочерние узлы.

## Примеры



Показывает, как клонировать составной узел.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Ниже представлены два способа клонирования составного узла.
// 1 -  Создать клон узла и также создать клон каждого из его дочерних узлов.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Создать клон узла только самого себя без каких-либо дочерних узлов.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```

## См. также

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
