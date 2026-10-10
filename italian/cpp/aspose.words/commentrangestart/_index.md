---
title: "classe Aspose::Words::CommentRangeStart"
linktitle: "CommentRangeStart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::CommentRangeStart. Indica l'inizio di una regione di testo a cui è associato un commento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words/commentrangestart/
---
## CommentRangeStart class


Indica l'inizio di una regione di testo a cui è associato un commento. Per saperne di più, visita l'articolo di documentazione [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class CommentRangeStart : public Aspose::Words::Node,
                          public Aspose::Words::IDisplaceableByCustomXml,
                          public Aspose::Words::INodeWithAnnotationId
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [Clone](../node/clone/)(bool) | Crea un duplicato del nodo. |
| [CommentRangeStart](./commentrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, int32_t) | Inizializza una nuova istanza di questa classe. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](../node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_Id](./get_id/)() const | Specifica l'identificatore del commento a cui è collegata questa regione. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Restituisce **true** se questo nodo può contenere altri nodi. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [CommentRangeStart](../nodetype/). |
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
| [set_Id](./set_id/)(int32_t) | Specifica l'identificatore del commento a cui è collegata questa regione. |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Per creare un commento ancorato a una regione di testo, è necessario creare un [Comment](../comment/) e poi creare [CommentRangeStart](./) e [CommentRangeEnd](../commentrangeend/) e impostare i loro identificatori allo stesso valore di [Id](../comment/get_id/).

[CommentRangeStart](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

## Vedi anche

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
