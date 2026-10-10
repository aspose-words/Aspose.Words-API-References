---
title: "Méthode Aspose::Words::Comment::RemoveReply"
linktitle: "RemoveReply"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Comment::RemoveReply. Supprime la réponse spécifiée à ce commentaire en C++."
type: docs
weight: 17000
url: /fr/cpp/aspose.words/comment/removereply/
---
## Comment::RemoveReply method


Supprime la réponse spécifiée à ce commentaire.

```cpp
void Aspose::Words::Comment::RemoveReply(const System::SharedPtr<Aspose::Words::Comment> &reply)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| réponse | const System::SharedPtr\<Aspose::Words::Comment\>\& | Le nœud de commentaire de la réponse à supprimer. |

## Exemples



Montre comment supprimer les réponses aux commentaires.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"Another reply");

ASSERT_EQ(2, comment->get_Replies()->get_Count());

// Voici deux façons de supprimer les réponses d'un commentaire.
// 1 -  Utilisez la méthode "RemoveReply" pour supprimer les réponses d'un commentaire individuellement :
comment->RemoveReply(comment->get_Replies()->idx_get(0));

ASSERT_EQ(1, comment->get_Replies()->get_Count());

// 2 -  Utilisez la méthode "RemoveAllReplies" pour supprimer toutes les réponses d'un commentaire en une fois :
comment->RemoveAllReplies();

ASSERT_EQ(0, comment->get_Replies()->get_Count());
```

## Voir aussi

* Class [Comment](../)
* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
