---
title: "Aspose::Words::Paragraph::get_ParentSection metodo"
linktitle: "get_ParentSection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::get_ParentSection metodo. Recupera la Sezione genitore del paragrafo in C++."
type: docs
weight: 23000
url: /it/cpp/aspose.words/paragraph/get_parentsection/
---
## Paragraph::get_ParentSection method


Recupera la [Section](../../section/) genitore del paragrafo.

```cpp
System::SharedPtr<Aspose::Words::Section> Aspose::Words::Paragraph::get_ParentSection()
```


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

* Class [Section](../../section/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
