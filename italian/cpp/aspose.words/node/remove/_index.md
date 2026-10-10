---
title: "Metodo Aspose::Words::Node::Remove"
linktitle: "Rimuovi"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Node::Remove. Si rimuove dal genitore in C++."
type: docs
weight: 20000
url: /it/cpp/aspose.words/node/remove/
---
## Node::Remove method


Rimuove se stesso dal genitore.

```cpp
void Aspose::Words::Node::Remove()
```


## Esempi



Mostra come eliminare tutte le forme con immagini da un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));

for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        shape->Remove();
    }
}

ASSERT_EQ(0, shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_HasImage();
}))));
```


Mostra come rimuovere tutti i nodi figlio di un tipo specifico da un nodo composito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Salva il nodo fratello successivo in una variabile nel caso volessimo spostarci dopo aver eliminato questo nodo.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // Il corpo di una sezione può contenere nodi Paragraph e Table.
    // Se il nodo è una Tabella, rimuovilo dal genitore.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```

## Vedi anche

* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
