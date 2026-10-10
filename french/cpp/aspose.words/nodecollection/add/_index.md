---
title: "Aspose::Words::NodeCollection::Add méthode"
linktitle: "Add"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::NodeCollection::Add méthode. Ajoute un nœud à la fin de la collection en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/nodecollection/add/
---
## NodeCollection::Add method


Ajoute un nœud à la fin de la collection.

```cpp
void Aspose::Words::NodeCollection::Add(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| nœud | const System::SharedPtr\<Aspose::Words::Node\>\& | Le nœud à ajouter à la fin de la collection. |
## Remarques


Le nœud est inséré en tant qu’enfant dans l’objet nœud à partir duquel la collection a été créée.

Si le nœud à insérer a été créé à partir d’un autre document, vous devez utiliser [ImportNode()](../) pour importer le nœud dans le document actuel. Le nœud importé peut alors être inséré dans le document actuel.

## Exemples



Montre comment préparer un nouveau nœud de section pour l'édition.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Un document vierge comprend une section, qui possède un corps, qui à son tour possède un paragraphe.
// Nous pouvons ajouter du contenu à ce document en ajoutant des éléments tels que des séquences de texte, des formes ou des tableaux à ce paragraphe.
ASSERT_EQ(Aspose::Words::NodeType::Section, doc->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(0)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(0)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

// Si nous ajoutons une nouvelle section de cette manière, elle n'aura pas de corps, ni aucun autre nœud enfant.
doc->get_Sections()->Add(System::MakeObject<Aspose::Words::Section>(doc));

ASSERT_EQ(0, doc->get_Sections()->idx_get(1)->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Exécutez la méthode "EnsureMinimum" pour ajouter un corps et un paragraphe à cette section afin de commencer à l'éditer.
doc->get_LastSection()->EnsureMinimum();

ASSERT_EQ(Aspose::Words::NodeType::Body, doc->get_Sections()->idx_get(1)->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, doc->get_Sections()->idx_get(1)->get_Body()->GetChild(Aspose::Words::NodeType::Any, 0, true)->get_NodeType());

doc->get_Sections()->idx_get(0)->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Voir aussi

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
