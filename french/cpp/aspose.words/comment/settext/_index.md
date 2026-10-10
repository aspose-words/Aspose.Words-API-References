---
title: "Aspose::Words::Comment::SetText méthode"
linktitle: "SetText"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Comment::SetText. Il s'agit d'une méthode pratique qui permet de définir facilement le texte du commentaire en C++."
type: docs
weight: 22000
url: /fr/cpp/aspose.words/comment/settext/
---
## Comment::SetText method


Il s'agit d'une méthode pratique qui permet de définir facilement le texte du commentaire.

```cpp
void Aspose::Words::Comment::SetText(const System::String &text)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| texte | const System::String\& | Le nouveau texte du commentaire. |
## Remarques


Cette méthode permet de définir rapidement le texte d'un commentaire à partir d'une chaîne. La chaîne peut contenir des sauts de paragraphe, ce qui créera des paragraphes de texte dans le commentaire en conséquence. Si vous souhaitez insérer des éléments plus complexes dans le commentaire, par exemple des signets ou des tableaux ou appliquer une mise en forme riche, vous devez alors utiliser les classes de nœuds appropriées pour construire le texte du commentaire.

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
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
