---
title: "Aspose::Words::Node::PreviousPreOrder méthode"
linktitle: "PreviousPreOrder"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Node::PreviousPreOrder méthode. Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre en C++."
type: docs
weight: 19000
url: /fr/cpp/aspose.words/node/previouspreorder/
---
## Node::PreviousPreOrder method


Obtient le nœud précédent selon l'algorithme de traversée d'arbre en pré-ordre.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::PreviousPreOrder(const System::SharedPtr<Aspose::Words::Node> &rootNode)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| rootNode | const System::SharedPtr\<Aspose::Words::Node\>\& | Le nœud supérieur (limite) du parcours. |

### ReturnValue

Nœud précédent en ordre pré-ordre. Null si le *rootNode* est atteint.

## Exemples



Montre comment parcourir l'arbre des nœuds du document en utilisant l'algorithme de parcours en pré‑ordre, et supprimer toute forme rencontrée contenant une image.
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

## Voir aussi

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
