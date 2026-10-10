---
title: "Aspose::Words::Section classe"
linktitle: "Sezione"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Section classe. Rappresenta una singola sezione in un documento. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 58000
url: /it/cpp/aspose.words/section/
---
## Section class


Rappresenta una singola sezione in un documento. Per saperne di più, visita l'articolo di documentazione [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class Section : public Aspose::Words::CompositeNode,
                public Aspose::Words::ISectionAttrSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Quando implementato in una classe derivata, chiama il metodo VisitXXXEnd del visitatore di documento specificato. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Quando implementato in una classe derivata, chiama il metodo VisitXXXStart del visitatore di documento specificato. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendContent](./appendcontent/)(const System::SharedPtr\<Aspose::Words::Section\>\&) | Inserisce una copia del contenuto della sezione di origine alla fine di questa sezione. |
| [ClearContent](./clearcontent/)() | Cancella la sezione. |
| [ClearHeadersFooters](./clearheadersfooters/)() | Cancella le intestazioni e i piè di pagina di questa sezione. |
| [ClearHeadersFooters](./clearheadersfooters/)(bool) | Cancella le intestazioni e i piè di pagina di questa sezione. |
| [Clone](./clone/)() | Crea un duplicato di questa sezione. |
| [Clone](../node/clone/)(bool) | Crea un duplicato del nodo. |
| [DeleteHeaderFooterShapes](./deleteheaderfootershapes/)() | Elimina tutte le forme (oggetti di disegno) dalle intestazioni e dai piè di pagina di questa sezione. |
| [EnsureMinimum](./ensureminimum/)() | Assicura che la sezione abbia [Body](./get_body/) con un [Paragraph](../paragraph/). |
| [get_Body](./get_body/)() | Restituisce il nodo figlio [Body](../body/) della sezione. |
| [get_Count](../compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](../node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_HeadersFooters](./get_headersfooters/)() | Fornisce l'accesso ai nodi delle intestazioni e dei piè di pagina della sezione. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [Section](../nodetype/). |
| [get_PageSetup](./get_pagesetup/)() | Restituisce un oggetto che rappresenta la configurazione della pagina e le proprietà della sezione. |
| [get_ParentNode](../node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_ProtectedForForms](./get_protectedforforms/)() | Vero se la sezione è protetta per i moduli. Quando una sezione è protetta per i moduli, gli utenti possono selezionare e modificare il testo solo nei campi modulo in Microsoft Word. |
| [get_Range](../node/get_range/)() | Restituisce un oggetto [Range](../range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
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
| [PrependContent](./prependcontent/)(const System::SharedPtr\<Aspose::Words::Section\>\&) | Inserisce una copia del contenuto della sezione di origine all'inizio di questa sezione. |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ottiene il nodo precedente secondo l'algoritmo di attraversamento dell'albero in pre-ordine. |
| [Remove](../node/remove/)() | Rimuove se stesso dal genitore. |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | Rimuove tutti i nodi figlio del nodo corrente. |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | Rimuove tutti i nodi discendenti [SmartTag](../../aspose.words.markup/smarttag/) del nodo corrente. |
| [Section](./section/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | Inizializza una nuova istanza della classe [Section](./). |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | Seleziona un elenco di nodi che corrispondono all'espressione XPath. |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | Seleziona il primo [Node](../node/) che corrisponde all'espressione XPath. |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Impostatore per [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ProtectedForForms](./set_protectedforforms/)(bool) | Setter per [Aspose::Words::Section::get_ProtectedForForms](./get_protectedforforms/). |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


[Section](./) can have one [Body](../body/) and maximum one [HeaderFooter](../headerfooter/) of each [HeaderFooterType](../headerfootertype/). [Body](../body/) and [HeaderFooter](../headerfooter/) nodes can be in any order inside [Section](./).

Una sezione valida minima deve contenere [Body](../body/) con un [Paragraph](../paragraph/).

Ogni sezione ha il proprio insieme di proprietà che specificano le dimensioni della pagina, l'orientamento, i margini ecc.

Puoi creare una copia di una sezione usando [Clone()](../node/clone/). La copia può essere inserita nello stesso documento o in uno diverso.

Per aggiungere, inserire o rimuovere un'intera sezione, inclusi interruzione di sezione e proprietà della sezione, utilizza i metodi dell'oggetto [Sections](../document/get_sections/).

Per copiare e inserire solo il contenuto della sezione escludendo l'interruzione di sezione e le proprietà della sezione, usa i metodi [AppendContent()](../) e [PrependContent()](../).

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
