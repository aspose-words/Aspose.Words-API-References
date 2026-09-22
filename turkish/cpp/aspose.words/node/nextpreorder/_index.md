---
title: "Aspose::Words::Node::NextPreOrder yöntemi"
linktitle: "NextPreOrder"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Node::NextPreOrder yöntemi. C++'ta ön sipariş ağaç dolaşım algoritmasına göre bir sonraki düğümü alır."
type: docs
weight: 18000
url: /tr/cpp/aspose.words/node/nextpreorder/
---
## Node::NextPreOrder method


Ön sipariş (pre-order) ağaç dolaşım algoritmasına göre bir sonraki düğümü alır.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::NextPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| rootNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Dolaşımın üst düğümü (sınır). |

### ReturnValue

Ön sipariş sırasındaki bir sonraki düğüm. *rootNode*'a ulaşılırsa null döner.

## Örnekler



Belgenin düğüm ağacını ön sipariş dolaşım algoritmasıyla nasıl gezileceğini ve karşılaşılan görüntülü şekilleri nasıl sileceğinizi gösterir.
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

## Ayrıca Bakınız

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
