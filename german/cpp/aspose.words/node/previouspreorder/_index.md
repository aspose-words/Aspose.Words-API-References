---
title: "Aspose::Words::Node::PreviousPreOrder Methode"
linktitle: "PreviousPreOrder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::PreviousPreOrder Methode. Gibt den vorherigen Knoten gemäß dem Pre-Order-Baumdurchlauf-Algorithmus in C++ zurück."
type: docs
weight: 19000
url: /de/cpp/aspose.words/node/previouspreorder/
---
## Node::PreviousPreOrder method


Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::PreviousPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| rootNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Der oberste Knoten (Grenze) der Traversierung. |

### ReturnValue

Vorheriger Knoten in Pre-Order-Reihenfolge. Null, wenn der *rootNode* erreicht wurde.

## Beispiele



Zeigt, wie man den Knotbaum des Dokuments mit dem Pre-Order-Durchlauf-Algorithmus traversiert und jede gefundene Form mit einem Bild löscht.
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

## Siehe auch

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
