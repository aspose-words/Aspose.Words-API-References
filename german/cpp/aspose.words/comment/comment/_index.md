---
title: "Aspose::Words::Comment::Comment Konstruktor"
linktitle: "Kommentar"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Comment::Comment Konstruktor. Initialisiert eine neue Instanz der Klasse Comment in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Initialisiert eine neue Instanz der Klasse [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Eigentümerdokument. |
## Hinweise


Wenn [Comment](../) erstellt wird, gehört es zum angegebenen Dokument, ist aber noch nicht Teil des Dokuments und [ParentNode](../../node/get_parentnode/) ist **null**.

Um [Comment](../) an das Dokument anzuhängen, verwenden Sie [InsertAfter1()</see> oder <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) im Absatz, in dem Sie den Kommentar einfügen möchten.

Nachdem Sie einen Kommentar erstellt haben, vergessen Sie nicht, seine [Author](../get_author/), [Initial](../get_initial/) und [DateTime](../get_datetime/) Eigenschaften festzulegen.

## Siehe auch

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


Initialisiert eine neue Instanz der Klasse [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Das Eigentümerdokument. |
| Autor | const System::String\& | Der Autorenname für den Kommentar. Darf nicht **null** sein. |
| initial | const System::String\& | Die Initialen des Autors für den Kommentar. Darf nicht **null** sein. |
| dateTime | System::DateTime | Datum und Uhrzeit für den Kommentar. |

## Beispiele



Zeigt, wie man einem Absatz einen Kommentar hinzufügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// In Microsoft Word können wir diesen Kommentar im Dokumentenkörper rechtsklicken, um ihn zu bearbeiten oder darauf zu antworten.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Siehe auch

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
