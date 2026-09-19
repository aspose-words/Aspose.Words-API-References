---
title: "Classe Aspose::Words::HeaderFooter"
linktitle: "HeaderFooter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::HeaderFooter. Rappresenta un contenitore per il testo dell'intestazione o del piè di pagina di una sezione. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 31000
url: /it/cpp/aspose.words/headerfooter/
---
## HeaderFooter class


Rappresenta un contenitore per il testo dell'intestazione o del piè di pagina di una sezione. Per saperne di più, visita l'articolo di documentazione [Working with Headers and Footers](https://docs.aspose.com/words/cpp/working-with-headers-and-footers/).

```cpp
class HeaderFooter : public Aspose::Words::Story
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitatore. |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitor per visitare la fine dell'intestazione. |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | Accetta un visitor per visitare l'inizio dell'intestazione. |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [AppendParagraph](../story/appendparagraph/)(const System::String\&) | Un metodo di scorciatoia che crea un oggetto [Paragraph](../paragraph/) con testo opzionale e lo aggiunge alla fine di questo oggetto. |
| [Clone](../node/clone/)(bool) | Crea un duplicato del nodo. |
| [DeleteShapes](../story/deleteshapes/)() | Elimina tutte le forme dal testo di questa storia. |
| [get_Count](../compositenode/get_count/)() | Ottiene il numero di figli immediati di questo nodo. |
| [get_CustomNodeId](../node/get_customnodeid/)() const | Specifica un identificatore personalizzato per il nodo. |
| virtual [get_Document](../node/get_document/)() const | Ottiene il documento a cui appartiene questo nodo. |
| [get_FirstChild](../compositenode/get_firstchild/)() const | Ottiene il primo figlio del nodo. |
| [get_FirstParagraph](../story/get_firstparagraph/)() override | Ottiene il primo paragrafo nella storia. |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | Restituisce **true** se questo nodo ha dei nodi figli. |
| [get_HeaderFooterType](./get_headerfootertype/)() | Ottiene il tipo di questa intestazione/piè di pagina. |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | Restituisce **true** poiché questo nodo può avere nodi figli. |
| [get_IsHeader](./get_isheader/)() | Vero se questo oggetto [HeaderFooter](./) è un'intestazione. |
| [get_IsLinkedToPrevious](./get_islinkedtoprevious/)() | Vero se questa intestazione o piè di pagina è collegata all'intestazione o piè di pagina corrispondente nella sezione precedente. |
| [get_LastChild](../compositenode/get_lastchild/)() const | Ottiene l'ultimo figlio del nodo. |
| [get_LastParagraph](../story/get_lastparagraph/)() override | Ottiene l'ultimo paragrafo nella storia. |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | Ottiene il nodo immediatamente successivo a questo nodo. |
| [get_NodeType](./get_nodetype/)() const override | Restituisce [HeaderFooter](../nodetype/). |
| [get_Paragraphs](../story/get_paragraphs/)() override | Ottiene una collezione di paragrafi che sono figli immediati della storia. |
| [get_ParentNode](../node/get_parentnode/)() | Ottiene il genitore immediato di questo nodo. |
| [get_ParentSection](./get_parentsection/)() | Ottiene la sezione padre di questa storia. |
| [get_PreviousSibling](../node/get_previoussibling/)() | Ottiene il nodo immediatamente precedente a questo nodo. |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | Restituisce un oggetto [Range](../range/) che rappresenta la porzione di un documento contenuta in questo nodo. |
| [get_StoryType](../story/get_storytype/)() override | Ottiene il tipo di questa storia. |
| [get_Tables](../story/get_tables/)() override | Ottiene una collezione di tabelle che sono figli immediati della storia. |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | Ottiene il primo antenato del [NodeType](../nodetype/) specificato. |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | Restituisce il nodo figlio N-esimo che corrisponde al tipo specificato. |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | Restituisce una collezione dinamica di nodi figlio che corrispondono al tipo specificato. |
| [GetEnumerator](../compositenode/getenumerator/)() override | Fornisce supporto per l'iterazione in stile foreach sui nodi figlio di questo nodo. |
| [GetText](../compositenode/gettext/)() override | Ottiene il testo di questo nodo e di tutti i suoi figli. |
| [GetType](./gettype/)() const override |  |
| [HeaderFooter](./headerfooter/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::HeaderFooterType) | Crea una nuova intestazione o piè di pagina del tipo specificato. |
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
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | Impostatore per [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/). |
| [set_IsLinkedToPrevious](./set_islinkedtoprevious/)(bool) | Impostatore per [Aspose::Words::HeaderFooter::get_IsLinkedToPrevious](./get_islinkedtoprevious/). |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | Esporta il contenuto del nodo in una stringa nel formato specificato. |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Esporta il contenuto del nodo in una stringa usando le opzioni di salvataggio specificate. |
| static [Type](./type/)() |  |
## Note


[HeaderFooter](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

[HeaderFooter](./) is a section-level node and can only be a child of [Section](../section/). There can only be one [HeaderFooter](./) of each [HeaderFooterType](./get_headerfootertype/) in a [Section](../section/).

Se [Section](../section/) non ha un [HeaderFooter](./) di un tipo specifico o il [HeaderFooter](./) non ha nodi figli, questa intestazione/piè di pagina è considerata collegata all'intestazione/piè di pagina dello stesso tipo della sezione precedente in Microsoft Word.

Quando [HeaderFooter](./) contiene almeno un [Paragraph](../paragraph/), non è più considerato collegato al precedente in Microsoft Word.

## Esempi



Mostra come creare un'intestazione e un piè di pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Crea un'intestazione e aggiungi un paragrafo ad essa. Il testo in quel paragrafo
// apparirà nella parte superiore di ogni pagina di questa sezione, sopra il testo principale.
auto header = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::HeaderPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(header);

System::SharedPtr<Aspose::Words::Paragraph> para = header->AppendParagraph(u"My header.");

ASSERT_TRUE(header->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

// Crea un piè di pagina e aggiungi un paragrafo ad esso. Il testo in quel paragrafo
// apparirà nella parte inferiore di ogni pagina di questa sezione, sotto il testo principale.
auto footer = System::MakeObject<Aspose::Words::HeaderFooter>(doc, Aspose::Words::HeaderFooterType::FooterPrimary);
doc->get_FirstSection()->get_HeadersFooters()->Add(footer);

para = footer->AppendParagraph(u"My footer.");

ASSERT_FALSE(footer->get_IsHeader());
ASSERT_TRUE(para->get_IsEndOfHeaderFooter());

ASPOSE_ASSERT_EQ(footer, para->get_ParentStory());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), para->get_ParentSection());
ASPOSE_ASSERT_EQ(footer->get_ParentSection(), header->get_ParentSection());

doc->Save(get_ArtifactsDir() + u"HeaderFooter.Create.docx");
```


Mostra come eliminare tutti i piè di pagina da un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Itera attraverso ogni sezione e rimuove i piè di pagina di ogni tipo.
for (auto&& section : System::IterateOver(doc->LINQ_OfType<System::SharedPtr<Aspose::Words::Section> >()))
{
    // Esistono tre tipi di intestazioni e piè di pagina.
    // 1 -  L'intestazione/piè di pagina "First", che appare solo nella prima pagina di una sezione.
    System::SharedPtr<Aspose::Words::HeaderFooter> footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterFirst);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression = footer;
    if (condExpression != nullptr)
    {
        condExpression->Remove();
    }

    // 2 -  L'intestazione/piè di pagina "Primary", che appare nelle pagine dispari.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression2 = footer;
    if (condExpression2 != nullptr)
    {
        condExpression2->Remove();
    }

    // 3 -  L'intestazione/piè di pagina "Even", che appare nelle pagine pari.
    footer = section->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::FooterEven);
    System::SharedPtr<Aspose::Words::HeaderFooter> condExpression3 = footer;
    if (condExpression3 != nullptr)
    {
        condExpression3->Remove();
    }

    ASSERT_EQ(0, section->get_HeadersFooters()->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> hf)>>([](System::SharedPtr<Aspose::Words::Node> hf) -> bool
    {
        return !(System::ExplicitCast<Aspose::Words::HeaderFooter>(hf))->get_IsHeader();
    }))));
}

doc->Save(get_ArtifactsDir() + u"HeaderFooter.RemoveFooters.docx");
```


Mostra come sostituire il testo nel piè di pagina di un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footer.docx");

System::SharedPtr<Aspose::Words::HeaderFooterCollection> headersFooters = doc->get_FirstSection()->get_HeadersFooters();
System::SharedPtr<Aspose::Words::HeaderFooter> footer = headersFooters->idx_get(Aspose::Words::HeaderFooterType::FooterPrimary);

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_MatchCase(false);
options->set_FindWholeWordsOnly(false);

int32_t currentYear = System::DateTime::get_Now().get_Year();
footer->get_Range()->Replace(u"(C) 2006 Aspose Pty Ltd.", System::String::Format(u"Copyright (C) {0} by Aspose Pty Ltd.", currentYear), options);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ReplaceText.docx");
```

## Vedi anche

* Class [Story](../story/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
