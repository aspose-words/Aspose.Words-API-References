---
title: PreferredWidthType Enum
linktitle: PreferredWidthType
articleTitle: PreferredWidthType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Tables.PreferredWidthType. Defina fácilmente el ancho de tablas y celdas para un formato preciso de documentos.
type: docs
weight: 7150
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
| Auto | `1` | No se especifica el ancho preferido. El ancho real de la tabla o celda se especifica mediante el ancho explícito o lo determinará automáticamente el algoritmo de diseño de tabla al mostrarla, según la configuración de ajuste automático de la tabla. |
| Percent | `2` | Mide el ancho del elemento actual usando un porcentaje especificado. |
| Points | `3` | Mide el ancho del elemento actual utilizando una cantidad específica de puntos (1/72 de pulgada). |

## Ejemplos

Muestra cómo verificar el tipo de ancho preferido y el valor de una celda de tabla.

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
