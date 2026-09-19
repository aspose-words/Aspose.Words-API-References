---
title: "Aspose::Words::Node::get_NodeType metodo"
linktitle: "get_NodeType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Node::get_NodeType metodo. Ottiene il tipo di questo nodo in C++."
type: docs
weight: 9000
url: /it/cpp/aspose.words/node/get_nodetype/
---
## Node::get_NodeType method


Ottiene il tipo di questo nodo.

```cpp
virtual Aspose::Words::NodeType Aspose::Words::Node::get_NodeType() const =0
```


## Esempi



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


Mostra come utilizzare la proprietà NextSibling di un nodo per enumerare i suoi figli immediati.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Paragraphs.docx");

for (System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_FirstChild(); node != nullptr; node = node->get_NextSibling())
{
    std::cout << std::endl;
    std::cout << System::String::Format(u"Node type: {0}", Aspose::Words::Node::NodeTypeToString(node->get_NodeType())) << std::endl;

    System::String contents = node->GetText().Trim();
    std::cout << (contents == System::String::Empty ? u"This node contains no text" : System::String::Format(u"Contents: \"{0}\"", node->GetText().Trim())) << std::endl;
}
```

## Vedi anche

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
