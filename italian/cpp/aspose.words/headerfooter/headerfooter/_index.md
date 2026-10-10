---
title: "Costruttore Aspose::Words::HeaderFooter::HeaderFooter"
linktitle: "HeaderFooter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Costruttore Aspose::Words::HeaderFooter::HeaderFooter. Crea una nuova intestazione o piè di pagina del tipo specificato in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/headerfooter/headerfooter/
---
## HeaderFooter::HeaderFooter constructor


Crea una nuova intestazione o piè di pagina del tipo specificato.

```cpp
Aspose::Words::HeaderFooter::HeaderFooter(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::HeaderFooterType headerFooterType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento proprietario. |
| headerFooterType | Aspose::Words::HeaderFooterType | Un valore [HeaderFooterType](../get_headerfootertype/) che specifica il tipo dell'intestazione o del piè di pagina. |
## Note


Quando [HeaderFooter](../) viene creato, appartiene al documento specificato, ma non è ancora parte del documento e [ParentNode](../../node/get_parentnode/) è **null**.

Per aggiungere [HeaderFooter](../) a una [Section](../../section/) utilizzare [InsertAfter1()</see>, <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../), oppure la proprietà e i metodi [HeadersFooters](../../section/get_headersfooters/) [Add()](../), [Insert()](../).

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

## Vedi anche

* Class [DocumentBase](../../documentbase/)
* Enum [HeaderFooterType](../../headerfootertype/)
* Class [HeaderFooter](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
