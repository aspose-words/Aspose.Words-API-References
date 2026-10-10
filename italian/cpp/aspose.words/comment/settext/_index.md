---
title: "Metodo Aspose::Words::Comment::SetText"
linktitle: "SetText"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Comment::SetText. Questo è un metodo di convenienza che consente di impostare facilmente il testo del commento in C++."
type: docs
weight: 22000
url: /it/cpp/aspose.words/comment/settext/
---
## Comment::SetText method


Questo è un metodo di convenienza che consente di impostare facilmente il testo del commento.

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| testo | const System::String\& | Il nuovo testo del commento. |
## Note


Questo metodo consente di impostare rapidamente il testo di un commento a partire da una stringa. La stringa può contenere interruzioni di paragrafo, creando di conseguenza paragrafi di testo nel commento. Se desideri inserire elementi più complessi nel commento, ad esempio segnalibri o tabelle o applicare formattazione ricca, devi utilizzare le classi nodo appropriate per costruire il testo del commento.

## Esempi



Mostra come aggiungere un commento a un documento e poi rispondere ad esso.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Posiziona il commento su un nodo nel corpo del documento.
// Questo commento apparirà nella posizione del suo paragrafo,
// al di fuori del margine destro della pagina, e con una linea tratteggiata che lo collega al suo paragrafo.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Aggiungi una risposta, che apparirà sotto il commento genitore.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// I commenti e le risposte sono entrambi nodi Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// I commenti che non rispondono ad altri commenti sono "di livello superiore". Non hanno commenti antenati.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Le risposte hanno un commento di livello superiore come antenato.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## Vedi anche

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
