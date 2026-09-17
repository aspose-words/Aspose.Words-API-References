---
title: "Aspose::Words::Comment::get_Author méthode"
linktitle: "get_Author"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Comment::get_Author méthode. Retourne ou définit le nom de l'auteur d'un commentaire en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words/comment/get_author/
---
## Comment::get_Author method


Renvoie ou définit le nom de l'auteur d'un commentaire.

```cpp
System::String Aspose::Words::Comment::get_Author() const
```

## Remarques


Ne peut pas être **null**.

La valeur par défaut est une chaîne vide.

## Exemples



Montre comment imprimer tous les commentaires d'un document et leurs réponses.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Comments.docx");

System::SharedPtr<Aspose::Words::NodeCollection> comments = doc->GetChildNodes(Aspose::Words::NodeType::Comment, true);

// Si un commentaire n'a aucun ancêtre, c'est un commentaire de niveau supérieur (« top-level ») contrairement à un commentaire de type réponse.
// Imprime tous les commentaires de niveau supérieur ainsi que les réponses éventuelles.
for (auto&& comment : comments->LINQ_OfType<System::SharedPtr<Aspose::Words::Comment> >()->LINQ_Where(static_cast<System::Func<System::SharedPtr<Aspose::Words::Comment>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Comment> c)>>([](System::SharedPtr<Aspose::Words::Comment> c) -> bool
{
    return c->get_Ancestor() == nullptr;
})))->LINQ_ToList())
{
    std::cout << "Top-level comment:" << std::endl;
    std::cout << System::String::Format(u"\t\"{0}\", by {1}", comment->GetText().Trim(), comment->get_Author()) << std::endl;
    std::cout << System::String::Format(u"Has {0} replies", comment->get_Replies()->get_Count()) << std::endl;
    for (auto&& commentReply : System::IterateOver<Aspose::Words::Comment>(comment->get_Replies()))
    {
        std::cout << System::String::Format(u"\t\"{0}\", by {1}", commentReply->GetText().Trim(), commentReply->get_Author()) << std::endl;
    }
    std::cout << std::endl;
}
```

## Voir aussi

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
