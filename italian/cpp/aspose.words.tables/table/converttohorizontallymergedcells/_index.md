---
title: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells metodo"
linktitle: "ConvertToHorizontallyMergedCells"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells metodo. Converte le celle unite orizzontalmente per larghezza in celle unite tramite HorizontalMerge in C++."
type: docs
weight: 7000
url: /it/cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


Converte le celle unite orizzontalmente per larghezza in celle unite tramite [HorizontalMerge](../../cellformat/get_horizontalmerge/).

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## Note


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

Quando una cella della tabella è unita tramite la proprietà di larghezza, [HorizontalMerge](../../cellformat/get_horizontalmerge/) è priva di senso, ma a volte avere i flag di unione è più comodo.

Utilizza questo metodo per trasformare le celle della tabella unite orizzontalmente per larghezza in celle unite tramite flag di unione.

## Esempi



Mostra come convertire le celle unite orizzontalmente per larghezza in celle unite tramite CellFormat.HorizontalMerge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table with merged cells.docx");

// Microsoft Word non scrive più i flag di unione, definendo le celle unite per larghezza.
// Aspose.Words per impostazione predefinita definisce solo 5 celle in una riga, e nessuna di esse ha il flag di unione orizzontale,
// anche se c'erano 7 celle nella riga prima che avvenisse l'unione orizzontale.
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
ASSERT_TRUE(row->get_Cells()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> c)>>([](System::SharedPtr<Aspose::Words::Node> c) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Tables::Cell>(c))->get_CellFormat()->get_HorizontalMerge() == Aspose::Words::Tables::CellMerge::None;
}))));

// Usa il metodo "ConvertToHorizontallyMergedCells" per convertire le celle unite orizzontalmente
// per la sua larghezza alla cella unita orizzontalmente tramite flag.
// Ora, abbiamo 7 celle, e alcune di esse hanno valori di unione orizzontale.
table->ConvertToHorizontallyMergedCells();
row = table->get_Rows()->idx_get(0);

ASSERT_EQ(7, row->get_Cells()->get_Count());

ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(0)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::First, row->get_Cells()->idx_get(1)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::Previous, row->get_Cells()->idx_get(2)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(3)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::First, row->get_Cells()->idx_get(4)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::Previous, row->get_Cells()->idx_get(5)->get_CellFormat()->get_HorizontalMerge());
ASSERT_EQ(Aspose::Words::Tables::CellMerge::None, row->get_Cells()->idx_get(6)->get_CellFormat()->get_HorizontalMerge());
```

## Vedi anche

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
