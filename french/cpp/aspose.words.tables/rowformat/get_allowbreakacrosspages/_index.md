---
title: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages method"
linktitle: "get_AllowBreakAcrossPages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages method. Vrai si le texte d'une ligne de tableau est autorisé à se diviser lors d'un saut de page en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.tables/rowformat/get_allowbreakacrosspages/
---
## RowFormat::get_AllowBreakAcrossPages method


Vrai si le texte d'une ligne de table est autorisé à se diviser à travers un saut de page.

```cpp
bool Aspose::Words::Tables::RowFormat::get_AllowBreakAcrossPages()
```


## Exemples



Montre comment désactiver la rupture des lignes entre les pages pour chaque ligne d'un tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table spanning two pages.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Définissez la propriété "AllowBreakAcrossPages" sur "false" pour conserver la ligne
// en un seul morceau si un tableau s'étend sur deux pages, ce qui se décompose le long de cette ligne.
// Si la ligne est trop grande pour tenir sur une page, Microsoft Word la déplacera vers la page suivante.
// Définissez la propriété "AllowBreakAcrossPages" sur "true" pour autoriser la ligne à se diviser sur deux pages.
for (auto&& row : System::IterateOver<Aspose::Words::Tables::Row>(table))
{
    row->get_RowFormat()->set_AllowBreakAcrossPages(allowBreakAcrossPages);
}

doc->Save(get_ArtifactsDir() + u"Table.AllowBreakAcrossPages.docx");
```

## Voir aussi

* Class [RowFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
