---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words para .NET
description: Document ExpandTableStylesToDirectFormatting método. Convierte el formato especificado en los estilos de tabla en formato directo en las tablas del documento en C#.
type: docs
weight: 590
url: /es/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Convierte el formato especificado en los estilos de tabla en formato directo en las tablas del documento.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Observaciones

Este método existe porque esta versión de Aspose.Words proporciona solo soporte limitado para los estilos de tabla (ver más abajo). Este método puede resultar útil cuando carga un documento DOCX o WordprocessingML que contiene tablas formateadas con estilos de tabla y necesita consultar el formato de tablas, celdas, párrafos o texto.

Esta versión de Aspose.Words proporciona soporte limitado para los estilos de tabla de la siguiente manera:

* Los estilos de tabla definidos en documentos DOCX o WordprocessingML se conservan como estilos de tabla al guardar el documento como DOCX o WordprocessingML.
* Los estilos de tabla definidos en documentos DOCX o WordprocessingML se convierten automáticamente al formato directo en tablas al guardar el documento en cualquier otro formato, renderizado o impresión.
* Los estilos de tabla definidos en documentos DOC se conservan como estilos de tabla cuando se guarda el documento solo como DOC.

## Ejemplos

Muestra cómo aplicar las propiedades del estilo de una tabla directamente a los elementos de la tabla.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Este método se refiere a propiedades de estilo de tabla como las que configuramos anteriormente.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
