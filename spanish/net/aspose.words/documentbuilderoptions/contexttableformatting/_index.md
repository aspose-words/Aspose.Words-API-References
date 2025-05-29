---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: Aspose.Words para .NET
description: Descubra la propiedad ContextTableFormatting en DocumentBuilderOptions. Asegúrese de que el formato de la tabla se mantenga independiente, mejorando la claridad y el estilo de su documento.
type: docs
weight: 20
url: /es/net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

Verdadero si el formato aplicado al contenido de la tabla no afecta el formato del contenido que le sigue. El valor predeterminado es`verdadero` .

```csharp
public bool ContextTableFormatting { get; set; }
```

## Ejemplos

Muestra cómo ignorar el formato de tabla para el contenido posterior.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Agrega contenido antes de la tabla.
// El tamaño de fuente predeterminado es 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Cambia el tamaño de fuente dentro de la tabla.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// Si ContextTableFormatting es verdadero, entonces el formato de tabla no se aplica al contenido posterior.
// Si ContextTableFormatting es falso, entonces el formato de tabla se aplica al contenido después.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Ver también

* class [DocumentBuilderOptions](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
