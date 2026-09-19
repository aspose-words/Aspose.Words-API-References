---
title: "Aspose::Words::Node::PreviousPreOrder metodo"
linktitle: "PreviousPreOrder"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Node::PreviousPreOrder metodo. Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in ordine pre-visita in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words/node/previouspreorder/
---
## Node::PreviousPreOrder method


Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::PreviousPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| rootNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Il nodo superiore (limite) dell'attraversamento. |

### ReturnValue

Nodo precedente nell'ordine pre-visita. Null se si è raggiunto il *rootNode*.

## Esempi



Mostra come attraversare l'albero dei nodi del documento usando l'algoritmo di attraversamento pre-ordine e eliminare qualsiasi forma incontrata con un'immagine.
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

## Vedi anche

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
