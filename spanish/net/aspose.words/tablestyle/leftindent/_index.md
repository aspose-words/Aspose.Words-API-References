---
title: TableStyle.LeftIndent
second_title: Referencia de API de Aspose.Words para .NET
description: TableStyle propiedad. Obtiene o establece el valor que representa la sangría izquierda de una tabla.
type: docs
weight: 90
url: /es/net/aspose.words/tablestyle/leftindent/
---
## TableStyle.LeftIndent property

Obtiene o establece el valor que representa la sangría izquierda de una tabla.

```csharp
public double LeftIndent { get; set; }
```

### Ejemplos

Muestra cómo establecer la posición de una mesa.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// A continuación se muestran dos formas de alinear una tabla horizontalmente.
// 1 - Usa la propiedad "Alineación" para alinearlo a una ubicación en la página, como el centro:
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// Insertar una tabla y aplicarle el estilo que creamos.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - Usa "LeftIndent" para especificar una sangría desde el margen izquierdo de la página:
tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle2");
tableStyle.LeftIndent = 55;
tableStyle.Borders.Color = Color.Green;
tableStyle.Borders.LineStyle = LineStyle.Single;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned according to left indent");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

doc.Save(ArtifactsDir + "Table.SetTableAlignment.docx");
```

### Ver también

* class [TableStyle](../)
* espacio de nombres [Aspose.Words](../../tablestyle/)
* asamblea [Aspose.Words](../../../)


