---
title: "Aspose::Words::Node::PreviousPreOrder metod"
linktitle: "PreviousPreOrder"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Node::PreviousPreOrder metod. Hämtar föregående nod enligt pre-order-trädtraverseringsalgoritmen i C++."
type: docs
weight: 19000
url: /sv/cpp/aspose.words/node/previouspreorder/
---
## Node::PreviousPreOrder method


Hämtar föregående nod enligt pre‑order‑trädtraverseringsalgoritmen.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::PreviousPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| rootNode | const System::SharedPtr\\<Aspose::Words::Node\\>\\& | Den översta noden (gräns) för traversering. |

### ReturnValue

Föregående nod i pre-order-ordning. Null om *rootNode* nås.

## Exempel



Visar hur man traverserar dokumentets nodträd med pre‑order‑traverseringsalgoritmen och tar bort alla former med en bild som påträffas.
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

## Se även

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
