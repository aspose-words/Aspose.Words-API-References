---
title: "Aspose::Words::Node::get_NodeType-Methode"
linktitle: "get_NodeType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node::get_NodeType-Methode. Ermittelt den Typ dieses Knotens in C++."
type: docs
weight: 9000
url: /de/cpp/aspose.words/node/get_nodetype/
---
## Node::get_NodeType method


Ermittelt den Typ dieses Knotens.

```cpp
virtual Aspose::Words::NodeType Aspose::Words::Node::get_NodeType() const =0
```


## Beispiele



Zeigt, wie alle Kindknoten eines bestimmten Typs aus einem zusammengesetzten Knoten entfernt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());

System::SharedPtr<Aspose::Words::Node> curNode = doc->get_FirstSection()->get_Body()->get_FirstChild();

while (curNode != nullptr)
{
    // Speichere den nächsten Geschwisterknoten in einer Variablen, falls wir nach dem Löschen dieses Knotens zu ihm wechseln möchten.
    System::SharedPtr<Aspose::Words::Node> nextNode = curNode->get_NextSibling();

    // Ein Abschnittsinhalt kann Paragraph‑ und Table‑Knoten enthalten.
    // Ist der Knoten eine Table, entferne ihn vom übergeordneten Element.
    if (curNode->get_NodeType() == Aspose::Words::NodeType::Table)
    {
        curNode->Remove();
    }

    curNode = nextNode;
}

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Table, true)->get_Count());
```


Zeigt, wie die NextSibling‑Eigenschaft eines Knotens verwendet wird, um seine unmittelbaren Kinder zu enumerieren.
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

## Siehe auch

* Enum [NodeType](../../nodetype/)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
