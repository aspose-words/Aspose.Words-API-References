---
title: "Aspose::Words::Notes::Footnote::Footnote costruttore"
linktitle: "Footnote"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Notes::Footnote::Footnote costruttore. Inizializza un'istanza della classe Footnote in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.notes/footnote/footnote/
---
## Footnote::Footnote constructor


Inizializza un'istanza della classe [Footnote](../).

```cpp
Aspose::Words::Notes::Footnote::Footnote(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Notes::FootnoteType footnoteType)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento proprietario. |
| footnoteType | Aspose::Words::Notes::FootnoteType | Un valore [FootnoteType](../get_footnotetype/) che specifica se si tratta di una nota a piè di pagina o di una nota finale. |
## Note


Quando viene creato il [Footnote](../), appartiene al documento specificato, ma non è ancora parte del documento e [ParentNode](../../../aspose.words/node/get_parentnode/) è **null**.

Per aggiungere il [Footnote](../) al documento, usa[InsertAfter1()</see> or <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) nel paragrafo in cui desideri inserire la nota a piè di pagina.

## Esempi



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

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
