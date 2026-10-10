---
title: "Méthode Aspose::Words::RevisionCollection::AcceptAll"
linktitle: "AcceptAll"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::RevisionCollection::AcceptAll. Accepte toutes les révisions de cette collection en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection::AcceptAll method


Accepte toutes les révisions de cette collection.

```cpp
void Aspose::Words::RevisionCollection::AcceptAll()
```


## Exemples



Montre comment comparer des documents.
```cpp
auto docOriginal = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docOriginal);
builder->Writeln(u"This is the original document.");

auto docEdited = System::MakeObject<Aspose::Words::Document>();
builder = System::MakeObject<Aspose::Words::DocumentBuilder>(docEdited);
builder->Writeln(u"This is the edited document.");

// Comparer des documents avec des révisions déclenchera une exception.
if (docOriginal->get_Revisions()->get_Count() == 0 && docEdited->get_Revisions()->get_Count() == 0)
{
    docOriginal->Compare(docEdited, u"authorName", System::DateTime::get_Now());
}

// Après la comparaison, le document original recevra une nouvelle révision
// pour chaque élément différent dans le document modifié.
for (auto&& r : System::IterateOver(docOriginal->get_Revisions()))
{
    std::cout << System::String::Format(u"Revision type: {0}, on a node of type \"{1}\"", r->get_RevisionType(), r->get_ParentNode()->get_NodeType()) << std::endl;
    std::cout << System::String::Format(u"\tChanged text: \"{0}\"", r->get_ParentNode()->GetText()) << std::endl;
}

// Accepter ces révisions transformera le document original en document modifié.
docOriginal->get_Revisions()->AcceptAll();

ASSERT_EQ(docOriginal->GetText(), docEdited->GetText());
```

## Voir aussi

* Class [RevisionCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
