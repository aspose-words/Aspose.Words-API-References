---
title: "Aspose::Words::CompositeNode::get_LastChild méthode"
linktitle: "get_LastChild"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CompositeNode::get_LastChild méthode. Obtient le dernier enfant du nœud en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words/compositenode/get_lastchild/
---
## CompositeNode::get_LastChild method


Obtient le dernier enfant du nœud.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::get_LastChild() const
```


## Exemples



Montre comment utiliser les méthodes de [Node](../../node/) et de [CompositeNode](../) pour supprimer une section avant la dernière section du document.
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

* Class [Node](../../node/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
