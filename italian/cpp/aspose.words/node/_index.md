---
title: "classe Aspose::Words::Node"
linktitle: "Node"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Node. Classe base per tutti i nodi di un documento Word. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 41000
url: /it/cpp/aspose.words/node/
---
## Node class


Classe base per tutti i nodi di un documento Word. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class Node : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accetta un visitatore. |
| [Clone](./clone/)(bool) | Crea un duplicato del nodo. |
| [get_CustomNodeId](./get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](./get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| virtual [get_IsComposite](./get_iscomposite/)() | Restituisce **true** se questo nodo può contenere altri nodi. |
| [get_NextNode](./get_nextnode/)() const |  |
| [get_NextSibling](./get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| virtual [get_NodeType](./get_nodetype/)() const | Ottiene il tipo di questo nodo. |
| [get_ParentNode](./get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_PreviousSibling](./get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](./get_prevnode/)() const |  |
| [get_Range](./get_range/)() | Restituisce un oggetto [Range](../range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [GetAncestor](./getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../nodetype/) specificato. |
| [GetAncestorOf](./getancestorof/)() |  |
| virtual [GetText](./gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](./isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](./nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](./nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PreviousPreOrder](./previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](./remove/)() | Rimuove se stesso dal genitore. |
| [set_CustomNodeId](./set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](./get_customnodeid/). |
| [set_NextNode](./set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](./set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](./setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](./tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](./tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Un documento è rappresentato come un albero di nodi, simile a DOM o XmlDocument.

Per ulteriori informazioni, vedi il pattern di progettazione Composite.

La classe [Node](./):

* Defines the child node interface.
* Defines the interface for visiting nodes.
* Provides default cloning capability.
* Implements parent node and owner document mechanisms.
* Implements access to sibling nodes.



## Esempi



Mostra come clonare un nodo composito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Paragraph> para = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

// Di seguito sono riportati due modi per clonare un nodo composito.
// 1 -  Crea una copia di un nodo e crea anche una copia di ciascuno dei suoi nodi figlio.
System::SharedPtr<Aspose::Words::Node> cloneWithChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(true);

ASSERT_TRUE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithChildren))->get_HasChildNodes());
ASSERT_EQ(u"Hello world!", cloneWithChildren->GetText().Trim());

// 2 -  Crea una copia di un nodo da solo, senza alcun figlio.
System::SharedPtr<Aspose::Words::Node> cloneWithoutChildren = System::ExplicitCast<Aspose::Words::Node>(para)->Clone(false);

ASSERT_FALSE((System::ExplicitCast<Aspose::Words::CompositeNode>(cloneWithoutChildren))->get_HasChildNodes());
ASSERT_EQ(System::String::Empty, cloneWithoutChildren->GetText().Trim());
```


Mostra come attraversare la collezione di nodi figlio di un nodo composito.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Aggiungi due run e una shape come nodi figlio al primo paragrafo di questo documento.
auto paragraph = System::ExplicitCast<Aspose::Words::Paragraph>(doc->GetChild(Aspose::Words::NodeType::Paragraph, 0, true));
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world! "));

auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Rectangle);
shape->set_Width(200);
shape->set_Height(200);
// Nota che 'CustomNodeId' non viene salvato in un file di output ed esiste solo durante la vita del nodo.
shape->set_CustomNodeId(100);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello again!"));

// Itera attraverso la collezione di figli immediati del paragrafo,
// e stampa tutti i run o le shape che troviamo al suo interno.
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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
