---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument class"
linktitle: "GlossaryDocument"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument class. Rappresenta l'elemento radice per un documento glossario all'interno di un documento Word. Un documento glossario è un archivio per voci AutoText, AutoCorrect e Building Blocks. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class


Rappresenta l'elemento radice per un documento glossario all'interno di un documento Word. Un documento glossario è un archivio per AutoText, voci AutoCorrect e Building Blocks. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class GlossaryDocument : public Aspose::Words::DocumentBase
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare la fine del documento Glossary. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare l'inizio del documento Glossary. |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/)() const | Ottiene o imposta la forma di sfondo del documento. Può essere **null**. |
| [get_BuildingBlocks](./get_buildingblocks/)() | Restituisce una collezione tipizzata che rappresenta tutti i building block nel documento glossario. |
| [get_Count](../../aspose.words/compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_Document](../../aspose.words/documentbase/get_document/)() const override | Ottiene questa istanza. |
| [get_FirstBuildingBlock](./get_firstbuildingblock/)() | Ottiene il primo building block nel documento glossario. |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FontInfos](../../aspose.words/documentbase/get_fontinfos/)() const | Fornisce l'accesso alle proprietà dei caratteri utilizzati in questo documento. |
| [get_FootnoteSeparators](../../aspose.words/documentbase/get_footnoteseparators/)() const | Fornisce l'accesso ai separatori di note a piè di pagina/note finali definiti nel documento. |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_LastBuildingBlock](./get_lastbuildingblock/)() | Ottiene l'ultimo building block nel documento glossario. |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_Lists](../../aspose.words/documentbase/get_lists/)() const | Fornisce l'accesso alla formattazione delle liste utilizzata nel documento. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeChangingCallback](../../aspose.words/documentbase/get_nodechangingcallback/)() | Chiamato quando un nodo viene inserito o rimosso nel documento. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce il valore [GlossaryDocument](../../aspose.words/nodetype/). |
| [get_PageColor](../../aspose.words/documentbase/get_pagecolor/)() | Ottiene o imposta il colore della pagina del documento. Questa proprietà è una versione semplificata di [BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_ResourceLoadingCallback](../../aspose.words/documentbase/get_resourceloadingcallback/)() const | Consente di controllare come vengono caricate le risorse esterne. |
| [get_Styles](../../aspose.words/documentbase/get_styles/)() const | Restituisce una raccolta di stili definiti nel documento. |
| [get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/)() const | Chiamato durante varie procedure di elaborazione del documento quando viene rilevato un problema che potrebbe causare perdita di fedeltà dei dati o della formattazione. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetBuildingBlock](./getbuildingblock/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery, const System::String\&, const System::String\&) | Trova un building block utilizzando la galleria, la categoria e il nome specificati. |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetText](../../aspose.words/compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importa un nodo da un altro documento al documento corrente. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione. |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione. |
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
| [set_BackgroundShape](../../aspose.words/documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Metodo set per [Aspose::Words::DocumentBase::get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../../aspose.words/documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Chiamato quando un nodo viene inserito o rimosso nel documento. |
| [set_PageColor](../../aspose.words/documentbase/set_pagecolor/)(System::Drawing::Color) | Metodo set per [Aspose::Words::DocumentBase::get_PageColor](../../aspose.words/documentbase/get_pagecolor/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](../../aspose.words/documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Consente di controllare come vengono caricate le risorse esterne. |
| [set_WarningCallback](../../aspose.words/documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Metodo set per [Aspose::Words::DocumentBase::get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Alcuni documenti, solitamente i modelli, possono contenere voci AutoText, AutoCorrect e/o Building Blocks (noti anche come *voci del documento glossario*, *parti del documento* *o* *building blocks*).

Per accedere ai blocchi di costruzione, è necessario caricare un documento in un oggetto [Document](../../aspose.words/document/). I blocchi di costruzione saranno disponibili tramite la proprietà [GlossaryDocument](../../aspose.words/document/get_glossarydocument/).

[GlossaryDocument](./) can contain any number of [BuildingBlock](../buildingblock/) objects. Each [BuildingBlock](../buildingblock/) represents one document part.

Corrisponde agli elementi **glossaryDocument** e **docParts** in OOXML.

## Vedi anche

* Class [DocumentBase](../../aspose.words/documentbase/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
