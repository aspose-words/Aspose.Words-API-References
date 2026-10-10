---
title: "Classe Aspose::Words::Markup::StructuredDocumentTagRangeStart"
linktitle: "StructuredDocumentTagRangeStart"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Markup::StructuredDocumentTagRangeStart. Rappresenta l'inizio di un tag di documento strutturato **intervallato** che accetta contenuto a più sezioni. Vedere anche StructuredDocumentTagRangeEnd. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.markup/structureddocumenttagrangestart/
---
## StructuredDocumentTagRangeStart class


Rappresenta l'inizio di un tag di documento strutturato **intervallato** che accetta contenuto a più sezioni. Vedere anche [StructuredDocumentTagRangeEnd](../structureddocumenttagrangeend/). Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagRangeStart : public Aspose::Words::Node,
                                        public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>,
                                        public Aspose::Words::Markup::IStructuredDocumentTag
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AppendChild](./appendchild/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Aggiunge il nodo specificato alla fine dell'intervallo stdContent. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_Appearance](./get_appearance/)() override | Ottiene o imposta l'aspetto del tag di documento strutturato. |
| [get_Color](./get_color/)() override | Ottiene o imposta il colore del tag di documento strutturato. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_Id](./get_id/)() override | Specifica un Id numerico persistente, univoco e di sola lettura per questo tag di documento strutturato. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Restituisce **true** se questo nodo può contenere altri nodi. |
| [get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/)() override | Specifica se il contenuto di questo tag di documento strutturato deve essere interpretato come testo segnaposto (invece del normale contenuto testuale all'interno del tag). Se impostato su **true**, questo stato verrà ripristinato (mostrando il testo segnaposto) all'apertura del documento. |
| [get_LastChild](./get_lastchild/)() | Restituisce l'ultimo figlio nell'intervallo stdContent. |
| [get_Level](./get_level/)() const override | Restituisce il livello al quale inizia questo intervallo di tag di documento strutturato nell'albero del documento. |
| [get_LockContentControl](./get_lockcontentcontrol/)() override | Quando impostato su **true**, questa proprietà impedirà a un utente di eliminare questo tag di documento strutturato. |
| [get_LockContents](./get_lockcontents/)() override | Quando impostato su **true**, questa proprietà impedirà a un utente di modificare i contenuti di questo tag di documento strutturato. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [StructuredDocumentTagRangeStart](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_Placeholder](./get_placeholder/)() override | Restituisce il [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenente il testo segnaposto che dovrebbe essere visualizzato quando i contenuti di questo tag di documento strutturato sono vuoti, l'elemento XML mappato associato è vuoto come specificato tramite l'elemento [XmlMapping](./get_xmlmapping/) o l'elemento [IsShowingPlaceholderText](./get_isshowingplaceholdertext/) è **true**. |
| [get_PlaceholderName](./get_placeholdername/)() override | Ottiene o imposta il Nome del [BuildingBlock](../../aspose.words.buildingblocks/buildingblock/) contenente il testo segnaposto. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_RangeEnd](./get_rangeend/)() | Specifica la fine dell'intervallo se il [StructuredDocumentTag](../structureddocumenttag/) è un tag di documento strutturato **intervallato**. Altrimenti restituisce **null**. |
| [get_SdtType](./get_sdttype/)() override | Restituisce il tipo di questo tag di documento strutturato. |
| [get_Tag](./get_tag/)() const override | Specifica un tag associato al nodo corrente del tag di documento strutturato. Non può essere **null**. |
| [get_Title](./get_title/)() const override | Specifica il nome descrittivo associato a questo tag di documento strutturato. Non può essere **null**. |
| [get_WordOpenXML](./get_wordopenxml/)() override | Ottiene una stringa che rappresenta l'XML contenuto nel nodo nel formato [FlatOpc](../../aspose.words/saveformat/). |
| [get_WordOpenXMLMinimal](./get_wordopenxmlminimal/)() | Ottiene una stringa che rappresenta l'XML contenuto nel nodo nel formato [FlatOpc](../../aspose.words/saveformat/). A differenza della proprietà [WordOpenXML](./get_wordopenxml/), questo metodo genera un documento semplificato che esclude tutte le parti non relative al contenuto. |
| [get_XmlMapping](./get_xmlmapping/)() override | Restituisce un oggetto che rappresenta la mappatura di questo intervallo di tag di documento strutturato ai dati XML in una parte XML personalizzata del documento corrente. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChildNodes](./getchildnodes/)(Aspose::Words::NodeType, bool) override | Restituisce una collezione live di nodi figlio che corrispondono ai tipi specificati. |
| [GetEnumerator](./getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../../aspose.words/node/remove/)() | Rimuove se stesso dal genitore. |
| [RemoveAllChildren](./removeallchildren/)() | Rimuove tutti i nodi compresi tra questo nodo di inizio intervallo e il nodo di fine intervallo. |
| [RemoveSelfOnly](./removeselfonly/)() override | Rimuove questo nodo di inizio intervallo e i corrispondenti nodi di fine intervallo del tag di documento strutturato, ma mantiene il suo contenuto all'interno dell'albero del documento. |
| [set_Appearance](./set_appearance/)(Aspose::Words::Markup::SdtAppearance) override | Setter per [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Appearance](./get_appearance/). |
| [set_Color](./set_color/)(System::Drawing::Color) override | Setter per [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Color](./get_color/). |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsShowingPlaceholderText](./set_isshowingplaceholdertext/)(bool) override | Setter per [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_IsShowingPlaceholderText](./get_isshowingplaceholdertext/). |
| [set_LockContentControl](./set_lockcontentcontrol/)(bool) override | Setter per [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContentControl](./get_lockcontentcontrol/). |
| [set_LockContents](./set_lockcontents/)(bool) override | Impostatore per [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_LockContents](./get_lockcontents/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PlaceholderName](./set_placeholdername/)(System::String) override | Impostatore per [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_PlaceholderName](./get_placeholdername/). |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Tag](./set_tag/)(System::String) override | Impostatore per [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Tag](./get_tag/). |
| [set_Title](./set_title/)(System::String) override | Impostatore per [Aspose::Words::Markup::StructuredDocumentTagRangeStart::get_Title](./get_title/). |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](./settemplateweakptr/)(uint32_t) override |  |
| [StructuredDocumentTagRangeStart](./structureddocumenttagrangestart/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Markup::SdtType) | Inizializza una nuova istanza della classe **Structured document tag range start**. |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |

## Esempi



Mostra come ottenere le proprietà dei tag di documento strutturato multi-sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## Vedi anche

* Class [Node](../../aspose.words/node/)
* Interface [IStructuredDocumentTag](../istructureddocumenttag/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
