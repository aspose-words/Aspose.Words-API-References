---
title: "Aspose::Words::Inline classe"
linktitle: "Inline"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Inline classe. Classe base per nodi di livello inline che possono avere formattazione dei caratteri associata, ma non possono avere nodi figli propri. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 36000
url: /it/cpp/aspose.words/inline/
---
## Inline class


Classe base per i nodi a livello inline che possono avere una formattazione dei caratteri associata, ma non possono avere nodi figli propri. Per saperne di più, visita l'articolo di documentazione [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/).

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | Accetta un visitatore. |
| [Clone](../node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](../node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_Font](./get_font/)() | Fornisce l'accesso alla formattazione del carattere di questo oggetto. |
| virtual [get_IsComposite](../node/get_iscomposite/)() | Restituisce **true** se questo nodo può contenere altri nodi. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Restituisce **true** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Restituisce **true** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| virtual [get_NodeType](../node/get_nodetype/)() const | Ottiene il tipo di questo nodo. |
| [get_ParentNode](../node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_ParentParagraph](./get_parentparagraph/)() | Recupera il [Paragraph](../paragraph/) genitore di questo nodo. |
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
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Una classe derivata da [Inline](./) può essere un figlio di [Paragraph](../paragraph/).

## Esempi



Mostra come determinare il tipo di revisione di un nodo inline.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// Quando modifichiamo il documento mentre l'opzione \"Track Changes\", trovata in Review -> Tracking,
// è attivata in Microsoft Word, le modifiche che applichiamo contano come revisioni.
// Durante la modifica di un documento usando Aspose.Words, possiamo iniziare a tracciare le revisioni tramite
// invocando il metodo \"StartTrackRevisions\" del documento e interrompendo il tracciamento usando il metodo \"StopTrackRevisions\".
// Possiamo accettare le revisioni per assimilarle nel documento
// oppure rifiutarle per modificare efficacemente la modifica proposta.
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// Il nodo genitore di una revisione è il run a cui la revisione si riferisce. Un Run è un nodo Inline.
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// Di seguito sono riportati cinque tipi di revisioni che possono segnalare un nodo Inline.
// 1 -  Una revisione "insert":
// Questa revisione si verifica quando inseriamo del testo mentre tracciamo le modifiche.
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  Una revisione "format":
// Questa revisione si verifica quando modifichiamo la formattazione del testo mentre tracciamo le modifiche.
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  Una revisione "move from":
// Quando evidenziamo del testo in Microsoft Word e lo trasciniamo in una posizione diversa nel documento
// mentre tracciamo le modifiche, compaiono due revisioni.
// La revisione "move from" è una copia del testo originale prima di spostarlo.
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  Una revisione "move to":
// La revisione "move to" è il testo che abbiamo spostato nella sua nuova posizione nel documento.
// "Move from" e "move to" appaiono in coppia per ogni revisione di spostamento che eseguiamo.
// Accettare una revisione di spostamento elimina la revisione "move from" e il suo testo,
// e conserva il testo della revisione "move to".
// Rifiutare una revisione di spostamento, al contrario, conserva la revisione "move from" ed elimina la revisione "move to".
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  Una revisione "delete":
// Questa revisione si verifica quando eliminiamo del testo mentre tracciamo le modifiche. Quando eliminiamo il testo in questo modo,
// rimarrà nel documento come revisione finché non accettiamo la revisione,
// che eliminerà definitivamente il testo, o rifiuteremo la revisione, che manterrà il testo eliminato al suo posto.
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## Vedi anche

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
