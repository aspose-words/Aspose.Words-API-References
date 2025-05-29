---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words para .NET
description: Transforme los estilos de tabla en formato directo con el método ExpandTableStylesToDirectFormatting, mejorando la apariencia de su documento sin esfuerzo.
type: docs
weight: 630
url: /es/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Convierte el formato especificado en los estilos de tabla en formato directo en las tablas del documento.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Observaciones

Este método existe porque esta versión de Aspose.Words ofrece compatibilidad limitada con estilos de tabla (ver más abajo). Este método puede ser útil al cargar un documento DOCX o WordprocessingML que contenga tablas formateadas con estilos de tabla y necesite consultar el formato de tablas, celdas, párrafos o texto.

Esta versión de Aspose.Words proporciona soporte limitado para estilos de tabla como se indica a continuación:

* Los estilos de tabla definidos en documentos DOCX o WordprocessingML se conservan como estilos de tabla al guardar el documento como DOCX o WordprocessingML.
* Los estilos de tabla definidos en documentos DOCX o WordprocessingML se convierten automáticamente al formato directo en las tablas cuando el documento se guarda en cualquier otro formato, se renderiza o se imprime.
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
