---
title: "classe Aspose::Words::Paragraph"
linktitle: "Paragraph"
second_title: "Riferimento API Aspose.Words per C++"
description: "classe Aspose::Words::Paragraph. Rappresenta un paragrafo di testo. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 47000
url: /it/cpp/aspose.words/paragraph/
---
## Paragraph class


Rappresenta un paragrafo di testo. Per saperne di più, visita l'articolo di documentazione [Working with Paragraphs](https://docs.aspose.com/words/cpp/working-with-paragraphs/).

```cpp
class Paragraph : public Aspose::Words::CompositeNode,
                  public Aspose::Words::IParaAttrSource,
                  public Aspose::Words::IRunAttrSource,
                  public Aspose::Words::Revisions::ITrackableNode
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare la fine del paragrafo del documento. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore per visitare l'inizio del paragrafo del documento. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendField](./appendfield/)(Aspose::Words::Fields::FieldType, bool) | Aggiunge un campo a questo paragrafo. |
| [AppendField](./appendfield/)(const System::String\&) | Aggiunge un campo a questo paragrafo. |
| [AppendField](./appendfield/)(const System::String\&, const System::String\&) | Aggiunge un campo a questo paragrafo. |
| [Clone](../node/clone/)(bool) | Crea un duplicato del nodo. |
| [get_BreakIsStyleSeparator](./get_breakisstyleseparator/)() | Vero se questa interruzione di paragrafo è un Separatore [Style](../style/). Un separatore di stile consente a un paragrafo di consistere in parti che hanno stili di paragrafo diversi. |
| [get_Count](../compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](../node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FrameFormat](./get_frameformat/)() | Fornisce l'accesso alle proprietà di formattazione del frame. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | Restituisce true se questo oggetto è stato eliminato in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsEndOfCell](./get_isendofcell/)() | Vero se questo paragrafo è l'ultimo paragrafo in una [Cell](../../aspose.words.tables/cell/); falso altrimenti. |
| [get_IsEndOfDocument](./get_isendofdocument/)() | Vero se questo paragrafo è l'ultimo paragrafo nell'ultima sezione del documento. |
| [get_IsEndOfHeaderFooter](./get_isendofheaderfooter/)() | Vero se questo paragrafo è l'ultimo paragrafo nell'[HeaderFooter](../headerfooter/) (storia del testo principale) di una [Section](../section/); falso altrimenti. |
| [get_IsEndOfSection](./get_isendofsection/)() | Vero se questo paragrafo è l'ultimo paragrafo nel [Body](../body/) (storia del testo principale) di una [Section](../section/); falso altrimenti. |
| [get_IsFormatRevision](./get_isformatrevision/)() | Restituisce true se la formattazione dell'oggetto è stata modificata in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsInCell](./get_isincell/)() | Vero se questo paragrafo è un figlio immediato di una [Cell](../../aspose.words.tables/cell/); falso altrimenti. |
| [get_IsInsertRevision](./get_isinsertrevision/)() | Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsListItem](./get_islistitem/)() | Vero quando il paragrafo è un elemento in un elenco puntato o numerato nella revisione originale. |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | Restituisce **true** se questo oggetto è stato spostato (eliminato) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | Restituisce **true** se questo oggetto è stato spostato (inserito) in Microsoft Word mentre il tracciamento delle modifiche era abilitato. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_ListFormat](./get_listformat/)() | Fornisce l'accesso alle proprietà di formattazione dell'elenco del paragrafo. |
| [get_ListLabel](./get_listlabel/)() | Ottiene un oggetto [ListLabel](./get_listlabel/) che fornisce l'accesso al valore di numerazione dell'elenco e alla formattazione per questo paragrafo. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [Paragraph](../nodetype/). |
| [get_ParagraphBreakFont](./get_paragraphbreakfont/)() | Fornisce l'accesso alla formattazione del carattere di interruzione di paragrafo. |
| [get_ParagraphFormat](./get_paragraphformat/)() | Fornisce l'accesso alle proprietà di formattazione del paragrafo. |
| [get_ParentNode](../node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_ParentSection](./get_parentsection/)() | Recupera la [Section](../section/) genitore del paragrafo. |
| [get_ParentStory](./get_parentstory/)() | Recupera la storia a livello di sezione genitore che può essere [Body](../body/) o [HeaderFooter](../headerfooter/). |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Restituisce un oggetto [Range](../range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_Runs](./get_runs/)() | Fornisce l'accesso alla collezione tipizzata di frammenti di testo all'interno del paragrafo. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../nodetype/) specificato. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEffectiveTabStops](./geteffectivetabstops/)() | Restituisce un array di tutte le tabulazioni applicate a questo paragrafo, incluse quelle applicate indirettamente da stili o elenchi. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetText](./gettext/)() override | Ottiene il testo di questo paragrafo includendo il carattere di fine paragrafo. |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Restituisce l'indice del nodo figlio specificato nell'array dei nodi figlio. |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertField](./insertfield/)(Aspose::Words::Fields::FieldType, bool, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Inserisce un campo in questo paragrafo. |
| [InsertField](./insertfield/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Inserisce un campo in questo paragrafo. |
| [InsertField](./insertfield/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | Inserisce un campo in questo paragrafo. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)() | Unisce le run con la stessa formattazione nel paragrafo. |
| [JoinRunsWithSameFormatting](./joinrunswithsameformatting/)(const System::SharedPtr\<Aspose::Words::JoinRunsOptions\>\&) | Unisce le run con la stessa formattazione nel paragrafo. |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo successivo secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | Un metodo di utilità che converte un valore enum di tipo nodo in una stringa leggibile dall'utente. |
| [Paragraph](./paragraph/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Inizializza una nuova istanza della classe [Paragraph](./). |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../node/remove/)() | Rimuove se stesso dal genitore. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Rimuove tutti i nodi discendenti [SmartTag](../../aspose.words.markup/smarttag/) del nodo corrente. |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Seleziona il primo [Node](../node/) che corrisponde all'espressione XPath. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Impostatore per [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


[Paragraph](./) is a block-level node and can be a child of classes derived from [Story](../story/) or [InlineStory](../inlinestory/).

[Paragraph](./) can contain any number of inline-level nodes and bookmarks.

L'elenco completo dei nodi figlio che possono comparire all'interno di un paragrafo è costituito da [BookmarkStart](../bookmarkstart/), [BookmarkEnd](../bookmarkend/), [FieldStart](../../aspose.words.fields/fieldstart/), [FieldSeparator](../../aspose.words.fields/fieldseparator/), [FieldEnd](../../aspose.words.fields/fieldend/), [FormField](../../aspose.words.fields/formfield/), [Comment](../comment/), [Footnote](../../aspose.words.notes/footnote/), [Run](../run/), [SpecialChar](../specialchar/), [Shape](../../aspose.words.drawing/shape/), [GroupShape](../../aspose.words.drawing/groupshape/), [SmartTag](../../aspose.words.markup/smarttag/).

Un paragrafo valido in Microsoft Word termina sempre con un carattere di interruzione di paragrafo e un paragrafo valido minimo consiste solo in un'interruzione di paragrafo. La classe [Paragraph](./) aggiunge automaticamente il carattere di interruzione di paragrafo appropriato alla fine e questo carattere non fa parte dei nodi figlio del [Paragraph](./), quindi un [Paragraph](./) può essere vuoto.

Non includere i caratteri di fine paragrafo [ParagraphBreak](../controlchar/paragraphbreak/) o di fine cella [Cell](../controlchar/cell/) all'interno del testo del paragrafo, poiché potrebbero rendere il paragrafo non valido quando il documento viene aperto in Microsoft Word.

## Esempi



Mostra come costruire manualmente un documento Aspose.Words.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un documento vuoto contiene una sezione, un corpo e un paragrafo.
// Chiama il metodo "RemoveAllChildren" per rimuovere tutti quei nodi,
// e otterrai un nodo documento senza figli.
doc->RemoveAllChildren();

// Questo documento ora non ha nodi figli compositi a cui possiamo aggiungere contenuti.
// Se desideriamo modificarlo, dovremo ripopolare la sua collezione di nodi.
// Per prima cosa, crea una nuova sezione, quindi aggiungila come figlio al nodo radice del documento.
auto section = System::MakeObject<Aspose::Words::Section>(doc);
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(section);

// Imposta alcune proprietà di configurazione della pagina per la sezione.
section->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::NewPage);
section->get_PageSetup()->set_PaperSize(Aspose::Words::PaperSize::Letter);

// Una sezione ha bisogno di un corpo, che conterrà e visualizzerà tutti i suoi contenuti
// sulla pagina tra l'intestazione e il piè di pagina della sezione.
auto body = System::MakeObject<Aspose::Words::Body>(doc);
section->AppendChild<System::SharedPtr<Aspose::Words::Body>>(body);

// Crea un paragrafo, imposta alcune proprietà di formattazione e quindi aggiungilo come figlio al corpo.
auto para = System::MakeObject<Aspose::Words::Paragraph>(doc);

para->get_ParagraphFormat()->set_StyleName(u"Heading 1");
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

body->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(para);

// Infine, aggiungi del contenuto al documento. Crea un run,
// imposta il suo aspetto e i suoi contenuti, e quindi aggiungilo come figlio al paragrafo.
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello World!");
run->get_Font()->set_Color(System::Drawing::Color::get_Red());
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

ASSERT_EQ(u"Hello World!", doc->GetText().Trim());

doc->Save(get_ArtifactsDir() + u"Section.CreateManually.docx");
```

## Vedi anche

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
