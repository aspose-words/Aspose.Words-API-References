---
title: "Méthode EnsureMinimum de Aspose::Words::Tables::Cell"
linktitle: "EnsureMinimum"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode EnsureMinimum de Aspose::Words::Tables::Cell. Si le dernier enfant n'est pas un paragraphe, crée et ajoute un paragraphe vide en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.tables/cell/ensureminimum/
---
## Cell::EnsureMinimum method


Si le dernier enfant n’est pas un paragraphe, crée et ajoute un paragraphe vide.

```cpp
void Aspose::Words::Tables::Cell::EnsureMinimum()
```


## Exemples



Montre comment s'assurer qu'un nœud cellule contient les nœuds nécessaires pour commencer à y ajouter du contenu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);
auto cell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
row->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(cell);

// Les cellules peuvent contenir des paragraphes avec des éléments typiques tels que des runs, des formes et même d'autres tableaux.
// Notre nouvelle cellule n'a aucun paragraphe, et nous ne pouvons pas y ajouter de contenus tels que des nœuds run et shape tant qu'elle n'en possède pas.
ASSERT_EQ(0, cell->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Appeler la méthode "EnsureMinimum" sur une cellule garantira que
// la cellule possède au moins un paragraphe vide, auquel nous pourrons ensuite ajouter du contenu.
cell->EnsureMinimum();
cell->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Voir aussi

* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
