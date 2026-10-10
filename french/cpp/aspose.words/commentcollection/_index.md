---
title: "Aspose::Words::CommentCollection class"
linktitle: "CommentCollection"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::CommentCollection class. Fournit un accès typé à une collection de nœuds Comment. Pour en savoir plus, consultez l’article de documentation en C++."
type: docs
weight: 12000
url: /fr/cpp/aspose.words/commentcollection/
---
## CommentCollection class


Fournit un accès typé à une collection de nœuds [Comment](../comment/). Pour en savoir plus, consultez l’article de documentation [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/).

```cpp
class CommentCollection : public Aspose::Words::NodeCollection
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [Add](../nodecollection/add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Ajoute un nœud à la fin de la collection. |
| [Clear](../nodecollection/clear/)() | Supprime tous les nœuds de cette collection et du document. |
| [Contains](../nodecollection/contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Détermine si un nœud se trouve dans la collection. |
| [get_Count](../nodecollection/get_count/)() | Obtient le nombre de nœuds dans la collection. |
| [GetEnumerator](../nodecollection/getenumerator/)() override | Fournit une itération simple de type "foreach" sur la collection de nœuds. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Récupère un [Comment](../comment/) à l’indice donné. |
| [IndexOf](../nodecollection/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Renvoie l'index basé sur zéro du nœud spécifié. |
| [Insert](../nodecollection/insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Insère un nœud dans la collection à l'index spécifié. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](../nodecollection/remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Supprime le nœud de la collection et du document. |
| [RemoveAt](../nodecollection/removeat/)(int32_t) | Supprime le nœud à l'index spécifié de la collection et du document. |
| [ToArray](../nodecollection/toarray/)() | Copie tous les nœuds de la collection dans un nouveau tableau de nœuds. |
| static [Type](./type/)() |  |

## Exemples



Montre comment marquer un commentaire comme "done".
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Insérez un commentaire pour signaler une erreur.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Les commentaires possèdent un indicateur "Done", qui est défini sur "false" par défaut.
// Si un commentaire suggère que nous apportions une modification dans le document,
// nous pouvons appliquer la modification, puis également définir l’indicateur "Done" par la suite pour indiquer la correction.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Les commentaires qui sont "done" se différencieront
// des éléments qui ne sont pas "terminés" avec une couleur de texte atténuée.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## Voir aussi

* Class [NodeCollection](../nodecollection/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
