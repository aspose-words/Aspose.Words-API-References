---
title: "Classe Aspose::Words::TextColumn"
linktitle: "TextColumn"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Classe Aspose::Words::TextColumn. Représente une seule colonne de texte. TextColumn est un membre de la collection TextColumnCollection. La collection TextColumn comprend toutes les colonnes d'une section d'un document. Pour en savoir plus, consultez l'article de documentation en C++."
type: docs
weight: 70000
url: /fr/cpp/aspose.words/textcolumn/
---
## TextColumn class


Représente une seule colonne de texte. [TextColumn](./) est un membre de la collection [TextColumnCollection](../textcolumncollection/). La collection [TextColumn](./) comprend toutes les colonnes d'une section d'un document. Pour en savoir plus, consultez l'article de documentation [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumn : public System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | Obtient ou définit l'espace entre cette colonne et la colonne suivante en points. Non requis pour la dernière colonne. |
| [get_Width](./get_width/)() | Obtient ou définit la largeur de la colonne de texte en points. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | Définisseur pour [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/). |
| [set_Width](./set_width/)(double) | Définisseur pour [Aspose::Words::TextColumn::get_Width](./get_width/). |
| static [Type](./type/)() |  |
## Remarques


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

Lorsqu'une nouvelle [TextColumn](./) est créée, sa largeur et son espacement sont définis à zéro.

## Exemples



Montre comment créer des colonnes à espacement irrégulier.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Déterminez la quantité d'espace dont nous disposons pour organiser les colonnes.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Définissez la première colonne comme étroite.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Définissez la deuxième colonne pour qu'elle occupe le reste de l'espace disponible à l'intérieur des marges de la page.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
