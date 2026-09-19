---
title: "Metodo Aspose::Words::Comment::get_Done"
linktitle: "get_Done"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Comment::get_Done. Ottiene o imposta il flag che indica che il commento è stato contrassegnato come completato in C++."
type: docs
weight: 8000
url: /it/cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


Ottiene o imposta il flag che indica che il commento è stato contrassegnato come completato.

```cpp
bool Aspose::Words::Comment::get_Done() const
```


## Esempi



Mostra come contrassegnare un commento come "done".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Inserisci un commento per evidenziare un errore.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// I commenti hanno un flag "Done", che è impostato su "false" per impostazione predefinita.
// Se un commento suggerisce di apportare una modifica all'interno del documento,
// possiamo applicare la modifica e poi impostare il flag "Done" per indicare la correzione.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// I commenti che sono "done" si differenzieranno
// da quelli che non sono "completati" con un colore del testo sbiadito.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Vedi anche

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
