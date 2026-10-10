---
title: "Aspose::Words::CompositeNode::get_Count méthode"
linktitle: "get_Count"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CompositeNode::get_Count méthode. Obtient le nombre d'enfants immédiats de ce nœud en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/compositenode/get_count/
---
## CompositeNode::get_Count method


Obtient le nombre d'enfants immédiats de ce nœud.

```cpp
int32_t Aspose::Words::CompositeNode::get_Count()
```


## Exemples



Montre comment ajouter, mettre à jour et supprimer des nœuds enfants dans la collection d'enfants d'un [CompositeNode](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vide, par défaut, contient un paragraphe.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Les nœuds composites tels que notre paragraphe peuvent contenir d'autres nœuds composites et en ligne comme enfants.
System::SharedPtr<Aspose::Words::Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = System::MakeObject<Aspose::Words::Run>(doc, u"Initial text. ");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(paragraphText);

// Créez trois nœuds de séquence supplémentaires.
auto run1 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 1. ");
auto run2 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 2. ");
auto run3 = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");

// Le corps du document n'affichera pas ces séquences tant que nous ne les insérons pas dans un nœud composite
// qui fait lui-même partie de l'arbre de nœuds du document, comme nous l'avons fait avec la première séquence.
// Nous pouvons déterminer où le contenu texte des nœuds que nous insérons
// apparaît dans le document en spécifiant un emplacement d'insertion relatif à un autre nœud du paragraphe.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Insérez la deuxième séquence dans le paragraphe devant la séquence initiale.
paragraph->InsertBefore<System::SharedPtr<Aspose::Words::Run>>(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Insérez la troisième séquence après la séquence initiale.
paragraph->InsertAfter<System::SharedPtr<Aspose::Words::Run>>(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Insérez la première séquence au début de la collection des nœuds enfants du paragraphe.
paragraph->PrependChild<System::SharedPtr<Aspose::Words::Run>>(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Nous pouvons modifier le contenu de la séquence en modifiant et en supprimant les nœuds enfants existants.
(System::ExplicitCast<Aspose::Words::Run>(paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(Aspose::Words::NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());
```

## Voir aussi

* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
