---
title: "Método Aspose::Words::Node::NextPreOrder"
linktitle: "NextPreOrder"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Node::NextPreOrder. Obtiene el siguiente nodo según el algoritmo de recorrido de árbol en preorden en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words/node/nextpreorder/
---
## Node::NextPreOrder method


Obtiene el nodo siguiente según el algoritmo de recorrido en preorden del árbol.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::NextPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| rootNode | const System::SharedPtr\<Aspose::Words::Node\>\& | El nodo superior (límite) del recorrido. |

### ReturnValue

Siguiente nodo en orden preorden. Nulo si se alcanza el *rootNode*.

## Ejemplos



Muestra cómo recorrer el árbol de nodos del documento usando el algoritmo de recorrido en preorden y eliminar cualquier forma encontrada con una imagen.
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

## Ver también

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
