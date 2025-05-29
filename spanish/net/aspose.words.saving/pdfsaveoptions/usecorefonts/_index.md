---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words para .NET
description: Optimice sus PDF con PdfSaveOptions. Controle la sustitución de fuentes TrueType como Arial y Times New Roman para mejorar la calidad del documento.
type: docs
weight: 330
url: /es/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

Obtiene o establece un valor que determina si se deben sustituir o no las fuentes TrueType Arial, Times New Roman, Courier New y Symbol por las fuentes principales de PDF Type 1.

```csharp
public bool UseCoreFonts { get; set; }
```

## Observaciones

El valor predeterminado es`FALSO` . Cuando este valor se establece en`verdadero` Las fuentes Arial, Times New Roman, Courier New y Symbol se reemplazan en el documento PDF con la fuente Type 1 principal correspondiente.

Es necesario que las fuentes PDF principales, o sus métricas de fuente y fuentes de sustitución adecuadas, estén disponibles para cualquier aplicación de visualización de PDF.

Esta configuración solo funciona con texto codificado ANSI (Windows-1252). El texto no ANSI se escribirá con la fuente TrueType incrustada, independientemente de esta configuración.

La compatibilidad con PDF/A y PDF/UA requiere que todas las fuentes estén incorporadas.`FALSO` El valor se utilizará automáticamente al guardar en PDF/A y PDF/UA.

Las fuentes principales no son compatibles al guardar en formato PDF 2.0.`FALSO` El valor se utilizará automáticamente al guardar en PDF 2.0.

Esta opción tiene una prioridad más alta que[`FontEmbeddingMode`](../fontembeddingmode/) opción.

## Ejemplos

Muestra cómo habilitar o deshabilitar la sustitución de fuentes PDF Tipo 1.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Crea un objeto "PdfSaveOptions" que podamos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Establezca la propiedad "UseCoreFonts" en "verdadero" para reemplazar algunas fuentes,
// incluyendo las dos fuentes en nuestro documento, con sus equivalentes PDF Tipo 1.
// Establezca la propiedad "UseCoreFonts" en "falso" para no aplicar fuentes PDF Tipo 1.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);
```

### Ver también

* class [PdfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
