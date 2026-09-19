---
title: "Aspose::Words::Notes::Footnote::get_FootnoteType metodo"
linktitle: "get_FootnoteType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::Footnote::get_FootnoteType metodo. Restituisce un valore che specifica se si tratta di una nota a piè di pagina o di una nota finale in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.notes/footnote/get_footnotetype/
---
## Footnote::get_FootnoteType method


Restituisce un valore che specifica se si tratta di una nota a piè di pagina o di una nota finale.

```cpp
Aspose::Words::Notes::FootnoteType Aspose::Words::Notes::Footnote::get_FootnoteType() const
```


## Esempi



Mostra la differenza tra note a piè di pagina e note finali.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Di seguito sono riportati due modi per aggiungere riferimenti numerati al testo. Entrambi questi riferimenti aggiungeranno un
// piccolo segno di riferimento in apice nella posizione in cui li inseriamo.
// Il segno di riferimento, per impostazione predefinita, è il numero indice del riferimento tra tutti i riferimenti nel documento.
// Ogni riferimento creerà anche una voce, che avrà lo stesso segno di riferimento del testo principale
// e il testo di riferimento, che passeremo al metodo \"InsertFootnote\" del costruttore di documenti.
// 1 -  Una nota a piè di pagina, la cui voce apparirà nella stessa pagina del testo a cui fa riferimento:
builder->Write(u"Footnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 -  Una nota finale, la cui voce apparirà alla fine del documento:
builder->Write(u"Endnote referenced main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> endnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote text, will appear at the very end of the document.");

builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakNewPage);

ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Footnote, footnote->get_FootnoteType());
ASSERT_EQ(Aspose::Words::Notes::FootnoteType::Endnote, endnote->get_FootnoteType());

doc->Save(get_ArtifactsDir() + u"InlineStory.FootnoteEndnote.docx");
```

## Vedi anche

* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
