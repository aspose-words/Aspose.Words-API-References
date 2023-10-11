---
title: Enum PreferredWidthType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Tables.PreferredWidthType enumeración. Especifica la unidad de medida para el ancho preferido de una tabla o celda.
type: docs
weight: 6300
url: /es/net/aspose.words.tables/preferredwidthtype/
---
## PreferredWidthType enumeration

Especifica la unidad de medida para el ancho preferido de una tabla o celda.

```csharp
public enum PreferredWidthType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | `1` | No se especifica el ancho preferido. El ancho real de la tabla o celda se especifica utilizando el ancho explícito o será determinado automáticamente por el algoritmo de diseño de la tabla cuando se muestre la tabla, dependiendo de la configuración de ajuste automático de la tabla. |
| Percent | `2` | Mide el ancho del elemento actual usando un porcentaje específico. |
| Points | `3` | Mida el ancho del elemento actual utilizando un número específico de puntos (1/72 de pulgada). |

### Ejemplos

Muestra cómo verificar el tipo de ancho preferido y el valor de una celda de una tabla.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### Ver también

* class [PreferredWidth](../preferredwidth/)
* espacio de nombres [Aspose.Words.Tables](../../aspose.words.tables/)
* asamblea [Aspose.Words](../../)


