---
title: HeightRule Enum
linktitle: HeightRule
articleTitle: HeightRule
second_title: Aspose.Words para .NET
description: Aspose.Words.HeightRule enumeración. Especifica la regla para determinar la altura de un objeto en C#.
type: docs
weight: 3130
url: /es/net/aspose.words/heightrule/
---
## HeightRule enumeration

Especifica la regla para determinar la altura de un objeto.

```csharp
public enum HeightRule
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| AtLeast | `0` | La altura será al menos la altura especificada en puntos. Crecerá, si es necesario, para acomodar todo el texto dentro de un objeto. |
| Exactly | `1` | La altura se especifica exactamente en puntos. Tenga en cuenta que si el texto no cabe dentro del objeto de esta altura, aparecerá truncado. |
| Auto | `2` | La altura crecerá automáticamente para acomodar todo el texto dentro de un objeto. |

## Ejemplos

Muestra cómo dar formato a filas con un generador de documentos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1.");

// Inicie una segunda fila y luego configure su altura. El constructor aplicará esta configuración a
// su fila actual, así como cualquier fila nueva que cree posteriormente.
builder.EndRow();

RowFormat rowFormat = builder.RowFormat;
rowFormat.Height = 100;
rowFormat.HeightRule = HeightRule.Exactly;

builder.InsertCell();
builder.Write("Row 2, cell 1.");
builder.EndTable();

// La primera fila no se vio afectada por la reconfiguración del relleno y aún mantiene los valores predeterminados.
Assert.AreEqual(0.0d, table.Rows[0].RowFormat.Height);
Assert.AreEqual(HeightRule.Auto, table.Rows[0].RowFormat.HeightRule);

Assert.AreEqual(100.0d, table.Rows[1].RowFormat.Height);
Assert.AreEqual(HeightRule.Exactly, table.Rows[1].RowFormat.HeightRule);

doc.Save(ArtifactsDir + "DocumentBuilder.SetRowFormatting.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
