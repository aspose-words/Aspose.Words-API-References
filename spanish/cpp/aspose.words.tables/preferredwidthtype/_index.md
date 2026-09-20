---
title: "Aspose::Words::Tables::PreferredWidthType enum"
linktitle: "PreferredWidthType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Tables::PreferredWidthType enum. Especifica la unidad de medida para el ancho preferido de una tabla o celda en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enum


Especifica la unidad de medida para el ancho preferido de una tabla o celda.

```cpp
enum class PreferredWidthType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | 1 | El ancho preferido no está especificado. El ancho real de la tabla o celda se especifica mediante el ancho explícito o se determinará automáticamente por el algoritmo de diseño de tabla cuando la tabla se muestre, dependiendo de la configuración de ajuste automático de la tabla. |
| Percent | 2 | Mide el ancho del elemento actual usando un porcentaje especificado. |
| Puntos | 3 | Mide el ancho del elemento actual usando un número especificado de puntos (1/72 de pulgada). |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
