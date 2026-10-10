---
title: "Aspose::Words::Comment::Comment costruttore"
linktitle: "Comment"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Comment::Comment costruttore. Inizializza una nuova istanza della classe Comment in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Inizializza una nuova istanza della classe [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento proprietario. |
## Note


Quando [Comment](../) viene creato, appartiene al documento specificato, ma non è ancora parte del documento e [ParentNode](../../node/get_parentnode/) è **null**.

Per aggiungere [Comment](../) al documento usa [InsertAfter1()</see> o <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) nel paragrafo in cui desideri inserire il commento.

Dopo aver creato un commento, non dimenticare di impostare le sue proprietà [Author](../get_author/), [Initial](../get_initial/) e [DateTime](../get_datetime/).

## Vedi anche

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


Inizializza una nuova istanza della classe [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Il documento proprietario. |
| autore | const System::String\& | Il nome dell'autore per il commento. Non può essere **null**. |
| iniziale | const System::String\& | Le iniziali dell'autore per il commento. Non possono essere **null**. |
| dateTime | System::DateTime | La data e l'ora del commento. |

## Esempi



Mostra come aggiungere un commento a un paragrafo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// In Microsoft Word, possiamo fare clic con il pulsante destro su questo commento nel corpo del documento per modificarlo o rispondere.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Vedi anche

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
