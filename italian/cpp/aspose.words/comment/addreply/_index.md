---
title: "Metodo Aspose::Words::Comment::AddReply"
linktitle: "AddReply"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Comment::AddReply. Aggiunge una risposta a questo commento in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/comment/addreply/
---
## Comment::AddReply method


Aggiunge una risposta a questo commento.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::AddReply(const System::String &author, const System::String &initial, System::DateTime dateTime, const System::String &text)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| autore | const System::String\& | Il nome dell'autore per la risposta. |
| iniziale | const System::String\& | Le iniziali dell'autore per la risposta. |
| dateTime | System::DateTime | La data e l'ora per la risposta. |
| testo | const System::String\& | Il testo della risposta. |

### ReturnValue

Il nodo [Comment](../) creato per la risposta.
## Note


A causa delle limitazioni esistenti di MS Office è consentito solo 1 livello di risposte nel documento.

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
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
