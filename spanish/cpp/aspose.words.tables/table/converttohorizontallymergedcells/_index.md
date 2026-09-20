---
title: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells método"
linktitle: "ConvertToHorizontallyMergedCells"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells método. Convierte celdas fusionadas horizontalmente por ancho a celdas fusionadas por HorizontalMerge en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.tables/table/converttohorizontallymergedcells/
---
## Table::ConvertToHorizontallyMergedCells method


Convierte celdas fusionadas horizontalmente por ancho a celdas fusionadas por [HorizontalMerge](../../cellformat/get_horizontalmerge/).

```cpp
void Aspose::Words::Tables::Table::ConvertToHorizontallyMergedCells()
```

## Observaciones


[Table](../) cells can be horizontally merged either using merge flags [HorizontalMerge](../../cellformat/get_horizontalmerge/) or using cell width [Width](../../cellformat/get_width/).

Cuando una celda de tabla está fusionada por la propiedad de ancho, [HorizontalMerge](../../cellformat/get_horizontalmerge/) no tiene sentido, pero a veces disponer de indicadores de fusión es una forma más conveniente.

Utilice este método para transformar celdas de tabla fusionadas horizontalmente por ancho en celdas fusionadas mediante indicadores de fusión.

## Ejemplos



Muestra cómo convertir celdas fusionadas horizontalmente por ancho en celdas fusionadas por CellFormat.HorizontalMerge.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table with merged cells.docx");

// Microsoft Word ya no escribe indicadores de fusión, definiendo las celdas fusionadas por ancho en su lugar.
// Aspose.Words por defecto define solo 5 celdas en una fila, y ninguna de ellas tiene el indicador de fusión horizontal,
// aunque había 7 celdas en la fila antes de que se realizara la fusión horizontal.
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Row> row = table->get_Rows()->idx_get(0);

ASSERT_EQ(5, row->get_Cells()->get_Count());
ASSERT_TRUE(row->get_Cells()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> c)>>([](System::SharedPtr<Aspose::Words::Node> c) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Tables::Cell>(c))->get_CellFormat()->get_HorizontalMerge() == Aspose::Words::Tables::CellMerge::None;
}))));

// Utilice el método "ConvertToHorizontallyMergedCells" para convertir celdas fusionadas horizontalmente
// por su ancho a la celda fusionada horizontalmente mediante banderas.
// Ahora, tenemos 7 celdas, y algunas de ellas tienen valores de fusión horizontal.
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

## Ver también

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
