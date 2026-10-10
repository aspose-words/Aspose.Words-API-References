---
title: "Aspose::Words::Comment::Comment constructeur"
linktitle: "Comment"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comment::Comment constructeur. Initialise une nouvelle instance de la classe Comment en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/comment/comment/
---
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) constructor


Initialise une nouvelle instance de la classe [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document propriétaire. |
## Remarques


Lorsque [Comment](../) est créé, il appartient au document spécifié, mais n'en fait pas encore partie et [ParentNode](../../node/get_parentnode/) est **null**.

Pour ajouter [Comment](../) au document, utilisez [InsertAfter1()</see> ou <see cref=\"Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\\>, System::SharedPtr\\<Aspose::Words::Node\\>)\">InsertBefore1()](../) sur le paragraphe où vous souhaitez insérer le commentaire.

Après avoir créé un commentaire, n'oubliez pas de définir ses propriétés [Author](../get_author/), [Initial](../get_initial/) et [DateTime](../get_datetime/).

## Voir aussi

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Comment::Comment(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


Initialise une nouvelle instance de la classe [Comment](../).

```cpp
Aspose::Words::Comment::Comment(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, const System::String &author, const System::String &initial, System::DateTime dateTime)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document propriétaire. |
| auteur | const System::String\& | Le nom de l'auteur du commentaire. Ne peut pas être **null**. |
| initiale | const System::String\& | Les initiales de l'auteur du commentaire. Ne peuvent pas être **null**. |
| dateTime | System::DateTime | La date et l'heure du commentaire. |

## Exemples



Montre comment ajouter un commentaire à un paragraphe.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// Dans Microsoft Word, nous pouvons cliquer avec le bouton droit sur ce commentaire dans le corps du document pour le modifier, ou y répondre.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Voir aussi

* Class [DocumentBase](../../documentbase/)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
