---
title: ConditionalStyle.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words para .NET
description: Formato claro y sin esfuerzo con el método ConditionalStyle ClearFormatting. ¡Simplifique su proceso de diseño y mejore la claridad de sus documentos hoy mismo!
type: docs
weight: 100
url: /es/net/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle.ClearFormatting method

Borra el formato de este estilo condicional.

```csharp
public void ClearFormatting()
```

## Ejemplos

Muestra cómo restablecer estilos de tabla condicionales.

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

// Establezca el estilo de tabla para colorear los bordes de la primera fila de la tabla en rojo.
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// Establezca el estilo de tabla para colorear los bordes de la última fila de la tabla en azul.
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// A continuación se muestran dos formas de utilizar el método "ClearFormatting" para borrar los estilos condicionales.
// 1 - Borrar los estilos condicionales de una parte específica de una tabla:
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - Borrar los estilos condicionales de toda la tabla:
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### Ver también

* class [ConditionalStyle](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
