---
title: "classe Aspose::Words::EditableRangeEnd"
linktitle: "EditableRangeEnd"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::EditableRangeEnd. Rappresenta la fine di un intervallo modificabile in un documento Word. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 25000
url: /it/cpp/aspose.words/editablerangeend/
---
## EditableRangeEnd class


Rappresenta la fine di un intervallo modificabile in un documento Word. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class EditableRangeEnd : public Aspose::Words::Node,
                         public Aspose::Words::IDisplaceableByCustomXml,
                         public Aspose::Words::INodeWithAnnotationId
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [Clone](../node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](../node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_EditableRangeStart](./get_editablerangestart/)() | Correlato [EditableRangeStart](../editablerangestart/), ricevuto per ID. |
| [get_Id](./get_id/)() const | Specifica l'identificatore dell'intervallo modificabile. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Restituisce **true** se questo nodo può contenere altri nodi. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [EditableRangeEnd](../nodetype/). |
| [get_ParentNode](../node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Restituisce un oggetto [Range](../range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../nodetype/) specificato. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../node/remove/)() | Rimuove se stesso dal genitore. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Impostatore per [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_Id](./set_id/)(int32_t) | Impostatore per [Aspose::Words::EditableRangeEnd::get_Id](./get_id/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Un intervallo modificabile completo in un documento Word è composto da un [EditableRangeStart](./get_editablerangestart/) e da un corrispondente [EditableRangeEnd](./) con lo stesso Id.

[EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./) are just markers inside a document that specify where the editable range starts and ends.

Usa la classe [EditableRange](../editablerange/) come una "facciata" per lavorare con un intervallo modificabile come un unico oggetto.


Attualmente gli intervalli modificabili sono supportati solo a livello inline, cioè all'interno di [Paragraph](../paragraph/), ma l'inizio e la fine dell'intervallo modificabile possono trovarsi in paragrafi diversi.

## Vedi anche

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
