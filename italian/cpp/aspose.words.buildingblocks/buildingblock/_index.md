---
title: "Classe Aspose::Words::BuildingBlocks::BuildingBlock"
linktitle: "BuildingBlock"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::BuildingBlocks::BuildingBlock. Rappresenta una voce del documento glossario come un Building Block, AutoText o una voce AutoCorrect. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 1000
url: /it/cpp/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class


Rappresenta una voce di documento glossario come un Building Block, AutoText o una voce AutoCorrect. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class BuildingBlock : public Aspose::Words::CompositeNode
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare la fine del [BuildingBlock](./). |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare l'inizio del [BuildingBlock](./). |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [BuildingBlock](./buildingblock/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | Inizializza una nuova istanza di questa classe. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_Behavior](./get_behavior/)() const | Specifica il comportamento che deve essere applicato quando il contenuto del blocco di costruzione viene inserito nel documento principale. |
| [get_Category](./get_category/)() const | Specifica la categorizzazione di secondo livello per il blocco di costruzione. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_Description](./get_description/)() const | Ottiene o imposta la descrizione associata a questo blocco di costruzione. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FirstSection](./get_firstsection/)() | Ottiene la prima sezione nel blocco di costruzione. |
| [get_Gallery](./get_gallery/)() const | Specifica la categorizzazione di primo livello per il blocco di costruzione ai fini della classificazione o dell'ordinamento dell'interfaccia utente. |
| [get_Guid](./get_guid/)() const | Ottiene o imposta un identificatore (un GUID a 128 bit) che identifica univocamente questo blocco di costruzione. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_LastSection](./get_lastsection/)() | Ottiene l'ultima sezione nel blocco di costruzione. |
| [get_Name](./get_name/)() const | Ottiene o imposta il nome di questo blocco di costruzione. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce il valore [BuildingBlock](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_Sections](./get_sections/)() | Restituisce una collezione che rappresenta tutte le sezioni nel blocco di costruzione. |
| [get_Type](./get_type/)() const | Specifica il tipo di blocco di costruzione. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../../aspose.words/node/remove/)() | Rimuove se stesso dal genitore. |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | Rimuove tutti i nodi discendenti [SmartTag](../../aspose.words.markup/smarttag/) del nodo corrente. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | Seleziona il primo [Node](../../aspose.words/node/) che corrisponde all'espressione XPath. |
| [set_Behavior](./set_behavior/)(Aspose::Words::BuildingBlocks::BuildingBlockBehavior) | Specifica il comportamento che deve essere applicato quando il contenuto del blocco di costruzione viene inserito nel documento principale. |
| [set_Category](./set_category/)(const System::String\&) | Impostatore per [Aspose::Words::BuildingBlocks::BuildingBlock::get_Category](./get_category/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_Description](./set_description/)(const System::String\&) | Impostatore per [Aspose::Words::BuildingBlocks::BuildingBlock::get_Description](./get_description/). |
| [set_Gallery](./set_gallery/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery) | Impostatore per [Aspose::Words::BuildingBlocks::BuildingBlock::get_Gallery](./get_gallery/). |
| [set_Guid](./set_guid/)(System::Guid) | Impostatore per [Aspose::Words::BuildingBlocks::BuildingBlock::get_Guid](./get_guid/). |
| [set_Name](./set_name/)(const System::String\&) | Impostatore per [Aspose::Words::BuildingBlocks::BuildingBlock::get_Name](./get_name/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Type](./set_type/)(Aspose::Words::BuildingBlocks::BuildingBlockType) | Impostatore per [Aspose::Words::BuildingBlocks::BuildingBlock::get_Type](./get_type/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


[BuildingBlock](./) can contain only [Section](../../aspose.words/section/) nodes.

[BuildingBlock](./) can only be a child of [GlossaryDocument](../glossarydocument/).

Puoi creare nuovi blocchi di costruzione e inserirli in un documento glossario. Puoi modificare o eliminare i blocchi di costruzione esistenti. Puoi copiare o spostare i blocchi di costruzione tra documenti. Puoi inserire il contenuto di un blocco di costruzione in un documento.

Corrisponde agli elementi **docPart**, **docPartPr** e **docPartBody** in OOXML.

## Vedi anche

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
