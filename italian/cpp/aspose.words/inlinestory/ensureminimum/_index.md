---
title: "Metodo Aspose::Words::InlineStory::EnsureMinimum"
linktitle: "EnsureMinimum"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::InlineStory::EnsureMinimum. Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/inlinestory/ensureminimum/
---
## InlineStory::EnsureMinimum method


Se l'ultimo figlio non è un paragrafo, crea e aggiunge un paragrafo vuoto.

```cpp
void Aspose::Words::InlineStory::EnsureMinimum()
```


## Esempi



Mostra come inserire i nodi [InlineStory](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// I nodi tabella hanno un metodo "EnsureMinimum()" che garantisce che la tabella abbia almeno una cella.
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// Possiamo inserire una tabella all'interno di una nota a piè di pagina, il che farà apparire la tabella nel piè di pagina della pagina di riferimento.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// Anche un InlineStory ha un metodo "EnsureMinimum()", ma in questo caso,
// assicura che l'ultimo figlio del nodo sia un paragrafo,
// per permetterci di fare clic e scrivere testo facilmente in Microsoft Word.
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// Modifica l'aspetto dell'ancora, che è il piccolo numero in apice
// nel testo principale che punta alla nota a piè di pagina.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// Tutti i nodi di storia inline hanno i rispettivi tipi di storia.
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// Un commento è un altro tipo di storia inline.
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// Il paragrafo genitore di un nodo di storia inline sarà quello del corpo principale del documento.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// Tuttavia, l'ultimo paragrafo è quello del contenuto testuale del commento,
// che sarà al di fuori del corpo principale del documento in una nuvoletta di dialogo.
// Un commento non avrà alcun nodo figlio per impostazione predefinita,
// quindi possiamo applicare il metodo EnsureMinimum() per inserire un paragrafo anche qui.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// Una volta ottenuto un paragrafo, possiamo spostare il builder per farlo e scrivere il nostro commento.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## Vedi anche

* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
