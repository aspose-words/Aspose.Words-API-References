---
title: "Aspose::Words::Tables::Row::EnsureMinimum méthode"
linktitle: "EnsureMinimum"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Row::EnsureMinimum méthode. Si le Row n'a aucune Cell, crée et ajoute une Cell en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.tables/row/ensureminimum/
---
## Row::EnsureMinimum method


Si le [Row](../) n'a aucune Cell, crée et ajoute une [Cell](../../cell/).

```cpp
void Aspose::Words::Tables::Row::EnsureMinimum()
```


## Exemples



Montre comment garantir qu'un nœud row contient les nœuds dont nous avons besoin pour commencer à y ajouter du contenu.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
auto row = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(row);

// Les Rows contiennent des cells, contenant des paragraphes avec des éléments typiques tels que des runs, des shapes et même d'autres tables.
// Notre nouvelle row ne possède aucun de ces nœuds, et nous ne pouvons pas y ajouter de contenu tant qu'il ne les possède pas.
ASSERT_EQ(0, row->GetChildNodes(Aspose::Words::NodeType::Any, true)->get_Count());

// Appeler la méthode "EnsureMinimum" sur une table garantira que
// La table possède au moins une cell avec un paragraphe vide.
row->EnsureMinimum();
row->get_FirstCell()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!"));
```

## Voir aussi

* Class [Row](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
