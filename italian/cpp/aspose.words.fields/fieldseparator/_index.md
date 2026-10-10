---
title: "Aspose::Words::Fields::FieldSeparator classe"
linktitle: "FieldSeparator"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::FieldSeparator classe. Rappresenta un separatore di campo Word che separa il codice del campo dal risultato del campo. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 90000
url: /it/cpp/aspose.words.fields/fieldseparator/
---
## FieldSeparator class


Rappresenta un separatore di campo Word che separa il codice del campo dal risultato del campo. Per saperne di più, visita l'articolo di documentazione [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) .

```cpp
class FieldSeparator : public Aspose::Words::Fields::FieldChar
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [Clone](../../aspose.words/node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_FieldType](../fieldchar/get_fieldtype/)() const | Restituisce il tipo del campo. |
| [get_Font](../../aspose.words/inline/get_font/)() | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | Restituisce **true** se questo nodo può contenere altri nodi. |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsDirty](../fieldchar/get_isdirty/)() const | Ottiene o imposta se il risultato corrente del campo non è più corretto (obsoleto) a causa di altre modifiche apportate al documento. |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsLocked](../fieldchar/get_islocked/)() const | Ottiene o imposta se il campo padre è bloccato (non dovrebbe ricalcolare il suo risultato). |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | Restituisce **true** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | Restituisce **true** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [FieldSeparator](../../aspose.words/nodetype/). |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | Recupera il [Paragraph](../../aspose.words/paragraph/) genitore di questo nodo. |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | Restituisce un oggetto [Range](../../aspose.words/range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../../aspose.words/nodetype/) specificato. |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](../fieldchar/getfield/)() | Restituisce un campo per il carattere di campo. |
| [GetText](../../aspose.words/specialchar/gettext/)() override | Ottiene il carattere speciale che questo nodo rappresenta. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../../aspose.words/node/remove/)() | Rimuove se stesso dal genitore. |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | Setter per [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/). |
| [set_IsDirty](../fieldchar/set_isdirty/)(bool) | Impostatore per [Aspose::Words::Fields::FieldChar::get_IsDirty](../fieldchar/get_isdirty/). |
| [set_IsLocked](../fieldchar/set_islocked/)(bool) | Impostatore per [Aspose::Words::Fields::FieldChar::get_IsLocked](../fieldchar/get_islocked/). |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


[FieldSeparator](./) is an inline-level node and represented by the [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) control character in the document.

[FieldSeparator](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

Un campo completo in un documento Microsoft Word è una struttura complessa composta da un carattere di inizio campo, codice di campo, carattere separatore di campo, risultato del campo e carattere di fine campo. Alcuni campi hanno solo il carattere di inizio campo, il codice di campo e il carattere di fine campo.

Per inserire facilmente un nuovo campo in un documento, utilizza il metodo [InsertField()](../).
## Vedi anche

* Class [FieldChar](../fieldchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
