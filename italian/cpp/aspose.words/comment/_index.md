---
title: "Aspose::Words::Comment class"
linktitle: "Comment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Comment class. Rappresenta un contenitore per il testo di un commento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words/comment/
---
## Comment class


Rappresenta un contenitore per il testo di un commento. Per saperne di più, visita l'articolo di documentazione [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare la fine del commento. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare l'inizio del commento. |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | Aggiunge una risposta a questo commento. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | Crea un duplicato del nodo. |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Inizializza una nuova istanza della classe [Comment](./). |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | Inizializza una nuova istanza della classe [Comment](./). |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto. |
| [get_Ancestor](./get_ancestor/)() | Restituisce l'oggetto [Comment](./) genitore. Restituisce **null** per i commenti di livello superiore. |
| [get_Author](./get_author/)() const | Restituisce o imposta il nome dell'autore per un commento. |
| [get_Count](../compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| [get_DateTime](./get_datetime/)() const | Ottiene la data e l'ora in cui è stato effettuato il commento. |
| [get_DateTimeUtc](./get_datetimeutc/)() | Ottiene la data e l'ora UTC in cui è stato effettuato il commento. |
| virtual [get_Document](../node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_Done](./get_done/)() const | Ottiene o imposta il flag che indica che il commento è stato contrassegnato come completato. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | Ottiene il primo paragrafo nella storia. |
| [get_Font](../inlinestory/get_font/)() | Fornisce l'accesso alla formattazione del carattere di ancoraggio di questo oggetto. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_Id](./get_id/)() const | Ottiene o imposta l'identificatore del commento. |
| [get_Initial](./get_initial/)() const | Restituisce o imposta le iniziali dell'utente associate a un commento specifico. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | Restituisce **true** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | Restituisce **true** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | Ottiene l'ultimo paragrafo nella storia. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [Comment](../nodetype/). |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | Ottiene una collezione di paragrafi che sono figli immediati della storia. |
| [get_ParentId](./get_parentid/)() const | Ottiene l'ID del commento genitore. Un valore di **%-1** indica che il commento non ha genitore. |
| [get_ParentNode](../node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | Recupera il [Paragraph](../paragraph/) genitore di questo nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Restituisce un oggetto [Range](../range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_Replies](./get_replies/)() | Restituisce una collezione di oggetti [Comment](./) che sono figli immediati del commento specificato. |
| [get_StoryType](./get_storytype/)() override | Restituisce [Comments](../storytype/). |
| [get_Tables](../inlinestory/get_tables/)() override | Ottiene una collezione di tabelle che sono figli immediati della storia. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../nodetype/) specificato. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetText](../compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
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
| [RemoveAllReplies](./removeallreplies/)() | Rimuove tutte le risposte a questo commento. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | Rimuove la risposta specificata a questo commento. |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Rimuove tutti i nodi discendenti [SmartTag](../../aspose.words.markup/smarttag/) del nodo corrente. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Seleziona il primo [Node](../node/) che corrisponde all'espressione XPath. |
| [set_Author](./set_author/)(const System::String\&) | Setter per [Aspose::Words::Comment::get_Author](./get_author/). |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Impostatore per [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_DateTime](./set_datetime/)(System::DateTime) | Ottiene la data e l'ora in cui è stato effettuato il commento. |
| [set_Done](./set_done/)(bool) | Setter per [Aspose::Words::Comment::get_Done](./get_done/). |
| [set_Id](./set_id/)(int32_t) | Setter per [Aspose::Words::Comment::get_Id](./get_id/). |
| [set_Initial](./set_initial/)(const System::String\&) | Setter per [Aspose::Words::Comment::get_Initial](./get_initial/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | Imposta l'ID del commento genitore. Un valore di **%-1** indica che il commento non ha genitore. |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | Questo è un metodo di convenienza che consente di impostare facilmente il testo del commento. |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


Un commento è un'annotazione ancorata a una regione di testo o a una posizione nel testo. Un commento può contenere una quantità arbitraria di contenuto a livello di blocco.

Se un oggetto [Comment](./) appare da solo, il commento è ancorato alla posizione dell'oggetto [Comment](./).

Per ancorare un commento a una regione di testo sono necessari tre oggetti: [Comment](./), [CommentRangeStart](../commentrangestart/) e [CommentRangeEnd](../commentrangeend/). Tutti e tre gli oggetti devono condividere lo stesso valore di [Id](./get_id/).

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## Esempi



Mostra come aggiungere un commento a un documento e poi rispondere ad esso.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Posiziona il commento su un nodo nel corpo del documento.
// Questo commento apparirà nella posizione del suo paragrafo,
// al di fuori del margine destro della pagina, e con una linea tratteggiata che lo collega al suo paragrafo.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Aggiungi una risposta, che apparirà sotto il commento genitore.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// I commenti e le risposte sono entrambi nodi Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// I commenti che non rispondono ad altri commenti sono "di livello superiore". Non hanno commenti antenati.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Le risposte hanno un commento di livello superiore come antenato.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```


Mostra come aggiungere un commento a un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// In Microsoft Word, possiamo fare clic con il pulsante destro su questo commento nel corpo del documento per modificarlo o rispondere.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Vedi anche

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
