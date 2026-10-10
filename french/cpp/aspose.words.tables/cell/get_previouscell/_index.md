---
title: "Aspose::Words::Tables::Cell::get_PreviousCell méthode"
linktitle: "get_PreviousCell"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Tables::Cell::get_PreviousCell méthode. Obtient le nœud Cell précédent en C++."
type: docs
weight: 12500
url: /fr/cpp/aspose.words.tables/cell/get_previouscell/
---
## Cell::get_PreviousCell method


Obtient le nœud [Cell](../) précédent.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::Tables::Cell::get_PreviousCell()
```


## Exemples



Montre comment énumérer toutes les cellules du tableau.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// Énumérez toutes les cellules du tableau.
for (System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_FirstRow(); row != nullptr; row = row->get_NextRow())
{
    for (System::SharedPtr<Aspose::Words::Tables::Cell> cell = row->get_FirstCell(); cell != nullptr; cell = cell->get_NextCell())
    {
        std::cout << cell->GetText() << std::endl;
    }
}
```

## Voir aussi

* Class [Cell](../)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
