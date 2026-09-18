---
title: "Aspose::Words::Node Klasse"
linktitle: "Node"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Node Klasse. Basisklasse für alle Knoten eines Word-Dokuments. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 41000
url: /de/cpp/aspose.words/node/
---
## Node class


Basisklasse für alle Knoten eines Word‑Dokuments. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class Node : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Akzeptiert einen Besucher. |
| [Clone](./clone/)(bool) | Erstellt ein Duplikat des Knotens. |
| [get_CustomNodeId](./get_customnodeid/)() const | Legt eine benutzerdefinierte Knotenkennung fest. |
| virtual [get_Document](./get_document/)() const | Ermittelt das Dokument, zu dem dieser Knoten gehört. |
| virtual [get_IsComposite](./get_iscomposite/)() | Liefert **true**, wenn dieser Knoten andere Knoten enthalten kann. |
| [get_NextNode](./get_nextnode/)() const |  |
| [get_NextSibling](./get_nextsibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar folgt. |
| virtual [get_NodeType](./get_nodetype/)() const | Ermittelt den Typ dieses Knotens. |
| [get_ParentNode](./get_parentnode/)() | Ermittelt den unmittelbaren Elternknoten dieses Knotens. |
| [get_PreviousSibling](./get_previoussibling/)() | Ermittelt den Knoten, der diesem Knoten unmittelbar vorausgeht. |
| [get_PrevNode](./get_prevnode/)() const |  |
| [get_Range](./get_range/)() | Gibt ein [Range](../range/)-Objekt zurück, das den Teil eines Dokuments darstellt, der in diesem Knoten enthalten ist. |
| [GetAncestor](./getancestor/)(Aspose::Words::NodeType) | Ermittelt den ersten Vorfahren des angegebenen [NodeType](../nodetype/). |
| [GetAncestorOf](./getancestorof/)() |  |
| virtual [GetText](./gettext/)() | Ermittelt den Text dieses Knotens und aller seiner Kindknoten. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](./isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](./nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den nächsten Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| static [NodeTypeToString](./nodetypetostring/)(Aspose::Words::NodeType) | Eine Hilfsmethode, die einen Enum‑Wert des Knotentyps in eine benutzerfreundliche Zeichenkette konvertiert. |
| [PreviousPreOrder](./previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ermittelt den vorherigen Knoten gemäß dem Preorder-Baumdurchlauf-Algorithmus. |
| [Remove](./remove/)() | Entfernt sich selbst vom übergeordneten Element. |
| [set_CustomNodeId](./set_customnodeid/)(int32_t) | Setter für [Aspose::Words::Node::get_CustomNodeId](./get_customnodeid/). |
| [set_NextNode](./set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](./set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](./setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](./tostring/)(Aspose::Words::SaveFormat) | Exportiert den Inhalt des Knotens in eine Zeichenkette im angegebenen Format. |
| [ToString](./tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Exportiert den Inhalt des Knotens in eine Zeichenkette unter Verwendung der angegebenen Speicheroptionen. |
| static [Type](./type/)() |  |
## Hinweise


Ein Dokument wird als Baum von Knoten dargestellt, ähnlich wie DOM oder XmlDocument.

Weitere Informationen finden Sie im Composite-Entwurfsmuster.

Die [Node](./) Klasse:

* Defines the child node interface.
* Defines the interface for visiting nodes.
* Provides default cloning capability.
* Implements parent node and owner document mechanisms.
* Implements access to sibling nodes.



## Beispiele



Zeigt, wie ein Composite-Knoten geklont wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Unten sind zwei Methoden zum Klonen eines Composite-Knotens aufgeführt.
// 1 -  Erstelle eine Kopie eines Knotens und erstelle ebenfalls eine Kopie jedes seiner Kindknoten.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Erstelle eine Kopie eines Knotens nur für sich selbst, ohne Kinder.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```


Zeigt, wie man durch die Sammlung von Kindknoten eines Composite-Knotens traversiert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Füge zwei Runs und eine Form als Kindknoten zum ersten Absatz dieses Dokuments hinzu.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Beachten Sie, dass die 'CustomNodeId' nicht in einer Ausgabedatei gespeichert wird und nur während der Lebensdauer des Knotens existiert.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Iterieren Sie durch die Sammlung unmittelbarer Kinder des Absatzes,
// und geben Sie alle Runs oder Shapes aus, die wir darin finden.
System::SharedPtr<Aspose::Words::NodeCollection> children = paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false);

ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, false)->get_Count());

for (auto&& child : System::IterateOver(children))
{
    switch (child->get_NodeType())
    {
        case Aspose::Words::NodeType::Run:
            std::cout << "Run contents:" << std::endl;
            std::cout << System::String::Format(u"\t\"{0}\"", child->GetText().Trim()) << std::endl;
            break;

        case Aspose::Words::NodeType::Shape:
        {
            auto childShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(child);
            std::cout << "Shape:" << std::endl;
            std::cout << System::String::Format(u"\t{0}, {1}x{2}", childShape->get_ShapeType(), childShape->get_Width(), childShape->get_Height()) << std::endl;
            ASSERT_EQ(100, shape->get_CustomNodeId());
            break;
        }

        default:
            break;
    }
}
```


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

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
