---
title: OutlineOptions.CreateMissingOutlineLevels
linktitle: CreateMissingOutlineLevels
articleTitle: CreateMissingOutlineLevels
second_title: Aspose.Words para .NET
description: OutlineOptions CreateMissingOutlineLevels propiedad. Obtiene o establece un valor que determina si se crean o no niveles de esquema faltantes cuando el documento se exporta  en C#.
type: docs
weight: 30
url: /es/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Obtiene o establece un valor que determina si se crean o no niveles de esquema faltantes cuando el documento se exporta .

El valor predeterminado para esta propiedad es`FALSO`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

## Ejemplos

Muestra cómo trabajar con niveles de esquema que no contienen ningún encabezado correspondiente al guardar un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar títulos que puedan servir como entradas TOC de los niveles 1 y 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Crea un objeto "PdfSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar cómo ese método convierte el documento a .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// El documento PDF de salida contendrá un esquema, que es una tabla de contenido que enumera los títulos en el cuerpo del documento.
// Al hacer clic en una entrada de este esquema nos llevará a la ubicación de su respectivo encabezado.
// Establece la propiedad "HeadingsOutlineLevels" en "5" para incluir todos los títulos de los niveles 5 e inferiores en el esquema.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Este documento contiene títulos de niveles 1 y 5, y ningún título con niveles de 2, 3 y 4.
// El documento PDF de salida considerará que "faltan" los niveles de esquema 2, 3 y 4.
// Establece la propiedad "CreateMissingOutlineLevels" en "true" para incluir todos los niveles que faltan en el esquema,
// dejando entradas de esquema en blanco ya que no hay encabezados utilizables.
// Establece la propiedad "CreateMissingOutlineLevels" en "false" para ignorar los niveles de esquema que faltan,
// y trate los encabezados del nivel 5 del esquema como de nivel 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Ver también

* class [OutlineOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
