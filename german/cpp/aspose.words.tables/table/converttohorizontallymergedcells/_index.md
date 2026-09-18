---
title: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells Methode"
linktitle: "ConvertToHorizontallyMergedCells"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells Methode. Konvertiert Zellen, die horizontal nach Breite zusammengeführt wurden, in Zellen, die durch HorizontalMerge zusammengeführt sind, in C++."
type: docs
weight: 7000
url: /de/cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


Konvertiert Zellen, die horizontal nach Breite zusammengeführt wurden, in Zellen, die durch [HorizontalMerge](../../cellformat/get_horizontalmerge/) zusammengeführt sind.

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## Hinweise


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

Wenn eine Tabellenzelle nach der Breite zusammengeführt wird, ist [HorizontalMerge](../../cellformat/get_horizontalmerge/) bedeutungslos, aber manchmal ist das Vorhandensein von Zusammenführungsflags ein praktischerer Ansatz.

Verwenden Sie diese Methode, um Tabellenzellen, die horizontal nach Breite zusammengeführt wurden, in Zellen umzuwandeln, die durch Zusammenführungsflags zusammengeführt sind.

## Beispiele



Zeigt, wie man Zellen, die horizontal nach Breite zusammengeführt wurden, in Zellen umwandelt, die durch CellFormat.HorizontalMerge zusammengeführt sind.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table with merged cells.docx");

// Microsoft Word schreibt keine Zusammenführungsflags mehr, sondern definiert zusammengeführte Zellen stattdessen nach Breite.
// Aspose.Words definiert standardmäßig nur 5 Zellen in einer Zeile, und keine von ihnen hat das horizontale Zusammenführungs-Flag,
// obwohl es vor dem horizontalen Zusammenführen 7 Zellen in der Zeile gab.
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
ASSERT_TRUE(row->get_Cells()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> c)>>([](System::SharedPtr<Aspose::Words::Node> c) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Tables::Cell>(c))->get_CellFormat()->get_HorizontalMerge() == Aspose::Words::Tables::CellMerge::None;
}))));

// Verwenden Sie die Methode "ConvertToHorizontallyMergedCells", um horizontal zusammengeführte Zellen zu konvertieren
// nach ihrer Breite in Zellen, die horizontal durch Flags zusammengeführt sind.
// Jetzt haben wir 7 Zellen, und einige von ihnen haben horizontale Zusammenführungswerte.
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

## Siehe auch

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
