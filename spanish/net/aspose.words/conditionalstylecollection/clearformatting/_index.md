---
title: ConditionalStyleCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words para .NET
description: ConditionalStyleCollection ClearFormatting método. Borra todos los estilos condicionales del estilo de tabla en C#.
type: docs
weight: 150
url: /es/net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

Borra todos los estilos condicionales del estilo de tabla.

```csharp
public void ClearFormatting()
```

## Ejemplos

Muestra cómo restablecer estilos de tablas condicionales.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("First row");
builder.EndRow();
builder.InsertCell();
builder.Write("Last row");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
table.Style = tableStyle;

// Establece el estilo de la tabla para colorear los bordes de la primera fila de la tabla en rojo.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Establece el estilo de la tabla para colorear los bordes de la última fila de la tabla en azul.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// A continuación se muestran dos formas de utilizar el método "ClearFormatting" para borrar los estilos condicionales.
// 1 - Borrar los estilos condicionales para una parte específica de una tabla:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Borrar los estilos condicionales para toda la tabla:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Ver también

* class [ConditionalStyleCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
