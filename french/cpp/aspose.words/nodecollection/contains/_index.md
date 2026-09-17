---
title: "Méthode Aspose::Words::NodeCollection::Contains"
linktitle: "Contains"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::NodeCollection::Contains. Détermine si un nœud se trouve dans la collection en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/nodecollection/contains/
---
## NodeCollection::Contains method


Détermine si un nœud se trouve dans la collection.

```cpp
bool Aspose::Words::NodeCollection::Contains(const System::SharedPtr<Aspose::Words::Node> &node)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| nœud | const System::SharedPtr\<Aspose::Words::Node\>\& | Le nœud à localiser. |

### ReturnValue

**true** if item is found in the collection; otherwise, **false**.
## Remarques


Cette méthode effectue une recherche linéaire ; par conséquent, le temps d'exécution moyen est proportionnel à [Count](../get_count/).

## Exemples



Montre comment travailler avec un [NodeCollection](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Ajoutez du texte au document en insérant des Runs à l'aide d'un DocumentBuilder.
builder->Write(u"Run 1. ");
builder->Write(u"Run 2. ");

// Chaque appel de la méthode "Write" crée un nouveau Run,
// qui apparaît ensuite dans la RunCollection du paragraphe parent.
System::SharedPtr<Aspose::Words::RunCollection> runs = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs();

ASSERT_EQ(2, runs->get_Count());

// Nous pouvons également insérer un nœud dans la RunCollection manuellement.
auto newRun = System::MakeObject<Aspose::Words::Run>(doc, u"Run 3. ");
runs->Insert(3, newRun);

ASSERT_TRUE(runs->Contains(newRun));
ASSERT_EQ(u"Run 1. Run 2. Run 3.", doc->GetText().Trim());

// Accédez aux runs individuels et supprimez-les pour retirer leur texte du document.
System::SharedPtr<Aspose::Words::Run> run = runs->idx_get(1);
runs->Remove(run);

ASSERT_EQ(u"Run 1. Run 3.", doc->GetText().Trim());
ASSERT_FALSE(System::TestTools::IsNull(run));
ASSERT_FALSE(runs->Contains(run));
```

## Voir aussi

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
