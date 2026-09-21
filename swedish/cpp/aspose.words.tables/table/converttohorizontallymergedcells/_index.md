---
title: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells‑metod"
linktitle: "ConvertToHorizontallyMergedCells"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells‑metod. Konverterar celler som är horisontellt sammanslagna efter bredd till celler som är sammanslagna med HorizontalMerge i C++."
type: docs
weight: 7000
url: /sv/cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


Konverterar celler som är horisontellt sammanslagna efter bredd till celler som är sammanslagna med [HorizontalMerge](../../cellformat/get_horizontalmerge/).

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## Anmärkningar


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

När en tabellcell är sammanslagen efter bredd är egenskapen [HorizontalMerge](../../cellformat/get_horizontalmerge/) meningslös, men ibland är det mer praktiskt att ha sammanslagningsflaggor.

Använd den här metoden för att omvandla tabellceller som är horisontellt sammanslagna efter bredd till celler som är sammanslagna med sammanslagningsflaggor.

## Exempel



Visar hur man konverterar celler som är horisontellt sammanslagna efter bredd till celler som är sammanslagna med CellFormat.HorizontalMerge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table with merged cells.docx");

// Microsoft Word skriver inte längre sammanslagningsflaggor, utan definierar sammanslagna celler efter bredd istället.
// Aspose.Words definierar som standard endast 5 celler i en rad, och ingen av dem har den horisontella sammanslagningsflaggan,
// även om det fanns 7 celler i raden innan den horisontella sammanslagningen ägde rum.
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
ASSERT_TRUE(row->get_Cells()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> c)>>([](System::SharedPtr<Aspose::Words::Node> c) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Tables::Cell>(c))->get_CellFormat()->get_HorizontalMerge() == Aspose::Words::Tables::CellMerge::None;
}))));

// Använd metoden "ConvertToHorizontallyMergedCells" för att konvertera celler som är horisontellt sammanslagna
// efter dess bredd till cellen som är horisontellt sammanslagen med flaggor.
// Nu har vi 7 celler, och några av dem har horisontella sammanslagningsvärden.
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

## Se även

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
