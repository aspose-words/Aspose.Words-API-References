---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.DocumentBuilderOptions para mejorar la creación de sus documentos con funciones personalizables para una experiencia de creación perfecta.
type: docs
weight: 670
url: /es/net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

Permite especificar opciones adicionales para el proceso de creación de documentos.

```csharp
public class DocumentBuilderOptions
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | Constructor predeterminado |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | Verdadero si el formato aplicado al contenido de la tabla no afecta el formato del contenido que le sigue. El valor predeterminado es`verdadero` . |
| [DesignMode](../../aspose.words/documentbuilderoptions/designmode/) { get; set; } | Corresponde al modo de diseño en Microsoft Word. |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
