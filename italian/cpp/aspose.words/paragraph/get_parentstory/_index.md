---
title: "Aspose::Words::Paragraph::get_ParentStory metodo"
linktitle: "get_ParentStory"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Paragraph::get_ParentStory metodo. Recupera la storia a livello di sezione genitore che può essere Body o HeaderFooter in C++."
type: docs
weight: 24000
url: /it/cpp/aspose.words/paragraph/get_parentstory/
---
## Paragraph::get_ParentStory method


Recupera la storia a livello di sezione genitore che può essere [Body](../../body/) o [HeaderFooter](../../headerfooter/).

```cpp
System::SharedPtr<Aspose::Words::Story> Aspose::Words::Paragraph::get_ParentStory()
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

* Class [Story](../../story/)
* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
