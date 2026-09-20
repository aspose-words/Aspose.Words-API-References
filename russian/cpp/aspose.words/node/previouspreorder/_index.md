---
title: "Aspose::Words::Node::PreviousPreOrder метод"
linktitle: "PreviousPreOrder"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Node::PreviousPreOrder метод. Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words/node/previouspreorder/
---
## Node::PreviousPreOrder method


Получает предыдущий узел согласно алгоритму обхода дерева в порядке предобхода.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::PreviousPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| rootNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Верхний узел (граница) обхода. |

### ReturnValue

Предыдущий узел в порядке предобхода. Null, если достигнут *rootNode*.

## Примеры



Показывает, как обходить дерево узлов документа, используя алгоритм предобхода, и удалять любые найденные фигуры с изображением.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

ASSERT_EQ(9, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));

System::SharedPtr<Aspose::Words::Node> curNode = doc;
while (curNode != nullptr)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->NextPreOrder(doc);

    if (curNode->PreviousPreOrder(doc) != nullptr && nextNode != nullptr)
    {
        ASPOSE_ASSERT_EQ(curNode, nextNode->PreviousPreOrder(doc));
    }

    if (curNode->get_NodeType() == Aspose::Words::NodeType::Shape && (System::ExplicitCast<Aspose::Words::Drawing::Shape>(curNode))->get_HasImage())
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));
```

## См. также

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
