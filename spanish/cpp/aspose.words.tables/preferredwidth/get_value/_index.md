---
title: "Aspose::Words::Tables::PreferredWidth::get_Value método"
linktitle: "get_Value"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::PreferredWidth::get_Value método. Obtiene el valor del ancho preferido. La unidad de medida se especifica en la propiedad Type en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.tables/preferredwidth/get_value/
---
## PreferredWidth::get_Value method


Obtiene el valor del ancho preferido. La unidad de medida se especifica en la propiedad [Type](../get_type/).

```cpp
double Aspose::Words::Tables::PreferredWidth::get_Value() const
```


## Ejemplos



Muestra cómo verificar el tipo y valor del ancho preferido de una celda de tabla.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
System::SharedPtr<Aspose::Words::Tables::Cell> firstCell = table->get_FirstRow()->get_FirstCell();

ASSERT_EQ(Aspose::Words::Tables::PreferredWidthType::Percent, firstCell->get_CellFormat()->get_PreferredWidth()->get_Type());
ASPOSE_ASSERT_EQ(11.16, firstCell->get_CellFormat()->get_PreferredWidth()->get_Value());
```

## Ver también

* Class [PreferredWidth](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
