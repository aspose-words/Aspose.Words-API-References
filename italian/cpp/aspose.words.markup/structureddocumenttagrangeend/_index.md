---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeEnd classe"
linktitle: "StructuredDocumentTagRangeEnd"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeEnd classe. Rappresenta la fine di un tag di documento strutturato a intervallo che accetta contenuto multi‑sezione. Vedi anche il nodo StructuredDocumentTagRangeStart. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words.markup/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd class


Rappresenta la fine di un tag di documento strutturato **ranged** che accetta contenuto multi‑sezione. Vedi anche il nodo [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/). Per saperne di più, visita l'articolo di documentazione [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/).

```cpp
class StructuredDocumentTagRangeEnd : public Aspose::Words::Node
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_Id](./get_id/)() const | Specifica un Id numerico unico, di sola lettura e persistente, per questo nodo **StructuredDocumentTagRange**. Il nodo corrispondente [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/) ha lo stesso [Id](../structureddocumenttagrangestart/get_id/). |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Restituisce **true** se questo nodo può contenere altri nodi. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [StructuredDocumentTagRangeEnd](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| virtual [GetText](../../aspose.words/node/gettext/)() | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../../aspose.words/node/remove/)() | Rimuove se stesso dal genitore. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, int32_t) | Inizializza una nuova istanza della classe **Structured document tag range end**. |
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
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
