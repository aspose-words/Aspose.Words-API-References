---
title: PreferredWidth.Value
second_title: Referencia de API de Aspose.Words para .NET
description: PreferredWidth propiedad. Obtiene el valor de ancho preferido. La unidad de medida se especifica en elType propiedad.
type: docs
weight: 50
url: /es/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

Obtiene el valor de ancho preferido. La unidad de medida se especifica en el[`Type`](../type/) propiedad.

```csharp
public double Value { get; }
```

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

* class [PreferredWidth](../)
* espacio de nombres [Aspose.Words.Tables](../../preferredwidth/)
* asamblea [Aspose.Words](../../../)


