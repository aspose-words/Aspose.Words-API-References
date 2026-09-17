---
title: "Aspose::Words::Tables::Table::EnsureMinimum méthode"
linktitle: "EnsureMinimum"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::EnsureMinimum méthode. Si le tableau n'a aucune ligne, crée et ajoute une Row en C++."
type: docs
weight: 8000
url: /fr/cpp/aspose.words.tables/table/ensureminimum/
---
## Table::EnsureMinimum method


Si le tableau n'a aucune ligne, crée et ajoute une [Row](../../row/).

```cpp
void Aspose::Words::Tables::Table::EnsureMinimum()
```


## Exemples



Montre comment s'assurer qu'un nœud de tableau contient les nœuds nécessaires pour ajouter du contenu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Les tableaux contiennent des lignes, qui contiennent des cellules, qui peuvent contenir des paragraphes
// avec des éléments typiques tels que des segments, des formes, et même d'autres tables.
// Notre nouveau tableau ne possède aucun de ces nœuds, et nous ne pouvons pas y ajouter de contenu tant qu'il ne les a pas.
ASSERT_EQ(0, table->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Appeler la méthode "EnsureMinimum" sur une table garantira que
// le tableau possède au moins une ligne et une cellule avec un paragraphe vide.
table->EnsureMinimum();
table->get_FirstRow()->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Voir aussi

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
