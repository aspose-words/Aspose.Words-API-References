---
title: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells yöntemi"
linktitle: "ConvertToHorizontallyMergedCells"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells yöntemi. Hücreleri genişlik ile yatay birleştirilmiş halden HorizontalMerge ile birleştirilmiş hâle C++'da dönüştürür."
type: docs
weight: 7000
url: /tr/cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


Hücreleri genişlik ile yatay birleştirilmiş halden [HorizontalMerge](../../cellformat/get_horizontalmerge/) ile birleştirilmiş hâle dönüştürür.

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## Açıklamalar


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

Tablo hücresi genişlik özelliğiyle birleştirildiğinde [HorizontalMerge](../../cellformat/get_horizontalmerge/) anlamsızdır, ancak bazen birleştirme bayraklarına sahip olmak daha kullanışlı bir yoldur.

Bu yöntemi, genişlik ile yatay birleştirilmiş tablo hücrelerini birleştirme bayraklarıyla birleştirilmiş hücrelere dönüştürmek için kullanın.

## Örnekler



Genişlik ile yatay birleştirilmiş hücrelerin CellFormat.HorizontalMerge ile birleştirilmiş hücrelere nasıl dönüştürüleceğini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table with merged cells.docx");

// Microsoft Word artık birleştirme bayrakları yazmaz, bunun yerine birleştirilmiş hücreleri genişlik ile tanımlar.
// Aspose.Words varsayılan olarak bir satırda yalnızca 5 hücre tanımlar ve bunların hiçbiri yatay birleştirme bayrağına sahip değildir,
// even though there were 7 cells in the row before the horizontal merging took place.
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
ASSERT_TRUE(row->get_Cells()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> c)>>([](System::SharedPtr<Aspose::Words::Node> c) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Tables::Cell>(c))->get_CellFormat()->get_HorizontalMerge() == Aspose::Words::Tables::CellMerge::None;
}))));

// Yatay birleştirilmiş hücreleri dönüştürmek için "ConvertToHorizontallyMergedCells" yöntemini kullanın
// bayraklarla yatay olarak birleştirilmiş hücreye genişliğiyle.
// Şimdi, 7 hücreye sahibiz ve bunların bazıları yatay birleştirme değerlerine sahip.
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

## Ayrıca Bakınız

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
