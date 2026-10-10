---
title: "Méthode Aspose::Words::Node::get_PreviousSibling"
linktitle: "get_PreviousSibling"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Node::get_PreviousSibling méthode. Obtient le nœud immédiatement précédant ce nœud en C++."
type: docs
weight: 11000
url: /fr/cpp/aspose.words/node/get_previoussibling/
---
## Node::get_PreviousSibling method


Obtient le nœud immédiatement précédent ce nœud.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Node::get_PreviousSibling()
```


## Exemples



Montre comment utiliser les méthodes de [Node](../) et [CompositeNode](../../compositenode/) pour supprimer une section avant la dernière section du document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Section 1 text.");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Writeln(u"Section 2 text.");

// Les deux sections sont sœurs l'une de l'autre.
auto lastSection = System::ExplicitCast<Aspose::Words::Section>(doc->get_LastChild());
auto firstSection = System::ExplicitCast<Aspose::Words::Section>(lastSection->get_PreviousSibling());

// Supprimez une section en fonction de sa relation de sœur avec une autre section.
if (lastSection->get_PreviousSibling() != nullptr)
{
    doc->RemoveChild<System::SharedPtr<Aspose::Words::Section>>(firstSection);
}

// La section que nous avons supprimée était la première, laissant le document avec seulement la seconde.
ASSERT_EQ(u"Section 2 text.", doc->GetText().Trim());
```

## Voir aussi

* Class [Node](../)
* Class [Node](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
