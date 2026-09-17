---
title: "Aspose::Words::Tables::Table::Table constructeur"
linktitle: "Table"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Table::Table constructeur. Initialise une nouvelle instance de la classe Table en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.tables/table/table/
---
## Table::Table constructor


Initialise une nouvelle instance de la classe [Table](../).

```cpp
Aspose::Words::Tables::Table::Table(const System::SharedPtr<Aspose::Words::DocumentBase> &doc)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | Le document propriétaire. |
## Remarques


Lorsque [Table](../) est créé, il appartient au document spécifié, mais n'en fait pas encore partie et [ParentNode](../../../aspose.words/node/get_parentnode/) est **null**.

Pour ajouter [Table](../) au document, utilisez [InsertAfter1()</see> ou <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) sur le récit où vous souhaitez insérer le tableau.

## Exemples



Montre comment créer un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
doc->get_FirstSection()->get_Body()->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);

// Les tables contiennent des lignes, qui contiennent des cellules, qui peuvent avoir des paragraphes
// avec des éléments typiques tels que des segments, des formes, et même d'autres tables.
// Appeler la méthode "EnsureMinimum" sur une table garantira que
// la table possède au moins une ligne, une cellule et un paragraphe.
auto firstRow = System::MakeObject<Aspose::Words::Tables::Row>(doc);
table->AppendChild<System::SharedPtr<Aspose::Words::Tables::Row>>(firstRow);

auto firstCell = System::MakeObject<Aspose::Words::Tables::Cell>(doc);
firstRow->AppendChild<System::SharedPtr<Aspose::Words::Tables::Cell>>(firstCell);

auto paragraph = System::MakeObject<Aspose::Words::Paragraph>(doc);
firstCell->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(paragraph);

// Ajoutez du texte à la première cellule de la première ligne de la table.
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");
paragraph->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->Save(get_ArtifactsDir() + u"Table.CreateTable.docx");
```

## Voir aussi

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
