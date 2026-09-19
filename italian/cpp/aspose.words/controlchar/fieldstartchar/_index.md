---
title: "Aspose::Words::ControlChar::FieldStartChar field"
linktitle: "FieldStartChar"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::ControlChar::FieldStartChar field. Carattere di inizio campo MS Word: (char)19 in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words/controlchar/fieldstartchar/
---
## FieldStartChar field


Carattere di inizio campo MS Word: (char)19.

```cpp
static constexpr char16_t Aspose::Words::ControlChar::FieldStartChar
```


## Esempi



Mostra come aggiungere vari caratteri di controllo a un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi uno spazio normale.
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::SpaceChar + u"After space.");

// Aggiungi un NBSP, che è uno spazio non interrotto.
// A differenza dello spazio normale, questo spazio non può avere un'interruzione di riga automatica nella sua posizione.
builder->Write(System::String(u"Before space.") + Aspose::Words::ControlChar::NonBreakingSpace() + u"After space.");

// Aggiungi un carattere di tabulazione.
builder->Write(System::String(u"Before tab.") + Aspose::Words::ControlChar::Tab() + u"After tab.");

// Aggiungi un'interruzione di riga.
builder->Write(System::String(u"Before line break.") + Aspose::Words::ControlChar::LineBreak() + u"After line break.");

// Aggiungi una nuova riga e avvia un nuovo paragrafo.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());
builder->Write(System::String(u"Before line feed.") + Aspose::Words::ControlChar::LineFeed() + u"After line feed.");
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// Il carattere di avanzamento riga ha due versioni.
ASSERT_EQ(Aspose::Words::ControlChar::LineFeed(), Aspose::Words::ControlChar::Lf());

// I ritorni a capo e gli avanzamenti riga possono essere rappresentati insieme da un unico carattere.
ASSERT_EQ(Aspose::Words::ControlChar::CrLf(), Aspose::Words::ControlChar::Cr() + Aspose::Words::ControlChar::Lf());

// Aggiungi un'interruzione di paragrafo, che avvierà un nuovo paragrafo.
builder->Write(System::String(u"Before paragraph break.") + Aspose::Words::ControlChar::ParagraphBreak() + u"After paragraph break.");
ASSERT_EQ(3, doc->get_FirstSection()->get_Body()->GetChildNodes(Aspose::Words::NodeType::Paragraph, true)->get_Count());

// Aggiungi un'interruzione di sezione. Questo non crea una nuova sezione o paragrafo.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
builder->Write(System::String(u"Before section break.") + Aspose::Words::ControlChar::SectionBreak() + u"After section break.");
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Aggiungi un'interruzione di pagina.
builder->Write(System::String(u"Before page break.") + Aspose::Words::ControlChar::PageBreak() + u"After page break.");

// Un'interruzione di pagina ha lo stesso valore di un'interruzione di sezione.
ASSERT_EQ(Aspose::Words::ControlChar::PageBreak(), Aspose::Words::ControlChar::SectionBreak());

// Inserisci una nuova sezione, quindi imposta il conteggio delle colonne a due.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc));
builder->MoveToSection(1);
builder->get_CurrentSection()->get_PageSetup()->get_TextColumns()->SetCount(2);

// Possiamo usare un carattere di controllo per segnare il punto in cui il testo passa alla colonna successiva.
builder->Write(System::String(u"Text at end of column 1.") + Aspose::Words::ControlChar::ColumnBreak() + u"Text at beginning of column 2.");

doc->Save(get_ArtifactsDir() + u"ControlChar.InsertControlChars.docx");

// Esistono controparti char e string per la maggior parte dei caratteri.
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Cell()), Aspose::Words::ControlChar::CellChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::NonBreakingSpace()), Aspose::Words::ControlChar::NonBreakingSpaceChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::Tab()), Aspose::Words::ControlChar::TabChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineBreak()), Aspose::Words::ControlChar::LineBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::LineFeed()), Aspose::Words::ControlChar::LineFeedChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ParagraphBreak()), Aspose::Words::ControlChar::ParagraphBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::SectionBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::PageBreak()), Aspose::Words::ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(Aspose::Words::ControlChar::ColumnBreak()), Aspose::Words::ControlChar::ColumnBreakChar);
```

## Vedi anche

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
