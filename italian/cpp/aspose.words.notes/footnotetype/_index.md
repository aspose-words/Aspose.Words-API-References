---
title: "Aspose::Words::Notes::FootnoteType enum"
linktitle: "FootnoteType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::FootnoteType enum. Specifica se si tratta di una nota a piè di pagina o di una nota finale in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.notes/footnotetype/
---
## FootnoteType enum


Specifica se si tratta di una nota a piè di pagina o di una nota finale.

```cpp
enum class FootnoteType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Footnote | 0 | L'oggetto è una nota a piè di pagina. |
| Nota finale | 1 | L'oggetto è una nota finale. |

## Note


Sia le note a piè di pagina che le note finali sono rappresentate da oggetti della classe [Footnote](./). Usa [FootnoteType](../footnote/get_footnotetype/) per distinguere tra note a piè di pagina e note finali.

## Esempi



Mostra come fare riferimento a del testo con una nota a piè di pagina e una nota finale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci del testo e contrassegnalo con una nota a piè di pagina con la proprietà IsAuto impostata su "true" per impostazione predefinita,
// in modo che il marcatore visualizzato nel testo principale sia numerato automaticamente a "1",
// e la nota a piè di pagina apparirà in fondo alla pagina.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Inserisci altro testo e contrassegnalo con una nota finale con un marcatore di riferimento personalizzato,
// che verrà usato al posto del numero "2" e imposterà "IsAuto" su false.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Le note a piè di pagina appaiono sempre in fondo al loro testo di riferimento,
// quindi questo interruzione di pagina non influenzerà la nota a piè di pagina.
// D'altra parte, le note finali sono sempre alla fine del documento
// in modo che questa interruzione di pagina spinga la nota finale alla pagina successiva.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```


Mostra come inserire e personalizzare le note a piè di pagina.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Aggiungi testo e riferiscilo con una nota a piè di pagina. Questa nota a piè di pagina inserirà un piccolo riferimento in apice
// dopo il testo a cui fa riferimento e creerà una voce sotto il testo principale in fondo alla pagina.
// Questa voce conterrà il marcatore di riferimento della nota a piè di pagina e il testo di riferimento,
// che passeremo al metodo "InsertFootnote" del costruttore del documento.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Se questa proprietà è impostata su "true", allora il marcatore di riferimento della nostra nota a piè di pagina
// sarà il suo indice tra tutte le note a piè di pagina della sezione.
// Questa è la prima nota a piè di pagina, quindi il marcatore di riferimento sarà "1".
ASSERT_TRUE(footnote->get_IsAuto());

// Possiamo spostare il costruttore del documento all'interno della nota a piè di pagina per modificare il suo testo di riferimento.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Possiamo impostare un marcatore di riferimento personalizzato che la nota a piè di pagina utilizzerà al posto del suo numero di indice.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// Un segnalibro con il flag "IsAuto" impostato su true mostrerà comunque il suo indice reale
// anche se i segnalibri precedenti mostrano marcatori di riferimento personalizzati, quindi il marcatore di riferimento di questo segnalibro sarà un "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## Vedi anche

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
