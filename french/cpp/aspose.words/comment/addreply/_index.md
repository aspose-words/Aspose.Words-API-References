---
title: "Méthode Aspose::Words::Comment::AddReply"
linktitle: "AddReply"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Comment::AddReply. Ajoute une réponse à ce commentaire en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/comment/addreply/
---
## Comment::AddReply method


Ajoute une réponse à ce commentaire.

```cpp
System::SharedPtr<Aspose::Words::Comment> Aspose::Words::Comment::AddReply(const System::String &author, const System::String &initial, System::DateTime dateTime, const System::String &text)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| auteur | const System::String\& | Le nom de l'auteur de la réponse. |
| initiale | const System::String\& | Les initiales de l'auteur de la réponse. |
| dateTime | System::DateTime | La date et l'heure de la réponse. |
| texte | const System::String\& | Le texte de la réponse. |

### ReturnValue

Le nœud [Comment](../) créé pour la réponse.
## Remarques


En raison des limitations existantes de MS Office, un seul niveau de réponses est autorisé dans le document.

## Exemples



Montre comment ajouter un commentaire à un document, puis y répondre.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// Placez le commentaire à un nœud dans le corps du document.
// Ce commentaire apparaîtra à l'emplacement de son paragraphe,
// en dehors de la marge droite de la page, et avec une ligne pointillée le reliant à son paragraphe.
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Ajoutez une réponse, qui apparaîtra sous le commentaire parent.
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// Les commentaires et les réponses sont tous deux des nœuds Comment.
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// Les commentaires qui ne répondent pas à d'autres commentaires sont "top-level". Ils n'ont aucun commentaire ancêtre.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// Les réponses ont un commentaire ancêtre de niveau supérieur.
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```

## Voir aussi

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
