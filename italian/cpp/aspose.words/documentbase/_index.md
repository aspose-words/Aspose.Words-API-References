---
title: "Aspose::Words::DocumentBase classe"
linktitle: "DocumentBase"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBase classe. Fornisce la classe base astratta per un documento principale e un documento di glossario di un documento Word. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words/documentbase/
---
## DocumentBase class


Fornisce la classe base astratta per un documento principale e un documento glossario di un documento Word. Per saperne di più, visita l'articolo di documentazione [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/).

```cpp
class DocumentBase : public Aspose::Words::CompositeNode
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accetta un visitatore. |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Quando implementato in una classe derivata, chiama il metodo VisitXXXEnd del visitatore di documento specificato. |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Quando implementato in una classe derivata, chiama il metodo VisitXXXStart del visitatore di documento specificato. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_BackgroundShape](./get_backgroundshape/)() const | Ottiene o imposta la forma di sfondo del documento. Può essere **null**. |
| [get_Count](../compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_Document](./get_document/)() const override | Ottiene questa istanza. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FontInfos](./get_fontinfos/)() const | Fornisce l'accesso alle proprietà dei caratteri utilizzati in questo documento. |
| [get_FootnoteSeparators](./get_footnoteseparators/)() const | Fornisce l'accesso ai separatori di note a piè di pagina/note finali definiti nel documento. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_Lists](./get_lists/)() const | Fornisce l'accesso alla formattazione delle liste utilizzata nel documento. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeChangingCallback](./get_nodechangingcallback/)() | Chiamato quando un nodo viene inserito o rimosso nel documento. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Ottiene il tipo di questo nodo. |
| [get_PageColor](./get_pagecolor/)() | Ottiene o imposta il colore della pagina del documento. Questa proprietà è una versione semplificata di [BackgroundShape](./get_backgroundshape/). |
| [get_ParentNode](../node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Restituisce un oggetto [Range](../range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | Consente di controllare come vengono caricate le risorse esterne. |
| [get_Styles](./get_styles/)() const | Restituisce una raccolta di stili definiti nel documento. |
| [get_WarningCallback](./get_warningcallback/)() const | Chiamato durante varie procedure di elaborazione del documento quando viene rilevato un problema che potrebbe causare perdita di fedeltà dei dati o della formattazione. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../nodetype/) specificato. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetText](../compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Importa un nodo da un altro documento al documento corrente. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione. |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | Importa un nodo da un altro documento al documento corrente con un'opzione per controllare la formattazione. |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../node/remove/)() | Rimuove se stesso dal genitore. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Rimuove tutti i nodi discendenti [SmartTag](../../aspose.words.markup/smarttag/) del nodo corrente. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Seleziona il primo [Node](../node/) che corrisponde all'espressione XPath. |
| [set_BackgroundShape](./set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | Metodo set per [Aspose::Words::DocumentBase::get_BackgroundShape](./get_backgroundshape/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Impostatore per [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](./set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | Chiamato quando un nodo viene inserito o rimosso nel documento. |
| [set_PageColor](./set_pagecolor/)(System::Drawing::Color) | Metodo set per [Aspose::Words::DocumentBase::get_PageColor](./get_pagecolor/). |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | Consente di controllare come vengono caricate le risorse esterne. |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Metodo set per [Aspose::Words::DocumentBase::get_WarningCallback](./get_warningcallback/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Aspose.Words rappresenta un documento Word come un albero di nodi. [DocumentBase](./) è un nodo radice dell'albero che contiene tutti gli altri nodi del documento.

[DocumentBase](./) also stores document-wide information such as [Styles](./get_styles/) and [Lists](./get_lists/) that the tree nodes might refer to.

## Esempi



Mostra come inizializzare le sottoclassi di [DocumentBase](./).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(doc).get_BaseType());

auto glossaryDoc = System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>();
doc->set_GlossaryDocument(glossaryDoc);

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(glossaryDoc).get_BaseType());
```

## Vedi anche

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
