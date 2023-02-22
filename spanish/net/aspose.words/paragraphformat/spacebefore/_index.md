---
title: ParagraphFormat.SpaceBefore
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Obtiene o establece la cantidad de espacio en puntos antes del párrafo.
type: docs
weight: 310
url: /es/net/aspose.words/paragraphformat/spacebefore/
---
## ParagraphFormat.SpaceBefore property

Obtiene o establece la cantidad de espacio (en puntos) antes del párrafo.

```csharp
public double SpaceBefore { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza cuando el argumento estaba fuera del rango de valores válidos. |

### Observaciones

No tiene efecto cuando[`SpaceBeforeAuto`](../spacebeforeauto/) es verdad.

Los valores válidos oscilan entre 0 y 1584 inclusive.

### Ejemplos

Muestra cómo configurar el espaciado automático de párrafos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aplique una gran cantidad de espacio antes y después de los párrafos que creará este constructor.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Establezca estas banderas en "verdadero" para aplicar espaciado automático,
// ignorando efectivamente el espaciado en las propiedades que establecimos arriba.
// Dejarlos como "falso" aplicará nuestro espaciado de párrafo personalizado.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Inserta dos párrafos que tendrán espacios arriba y abajo y guarda el documento.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

Muestra cómo no aplicar espacios entre párrafos con el mismo estilo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aplique una gran cantidad de espacio antes y después de los párrafos que creará este constructor.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Establecer el indicador "NoSpaceBetweenParagraphsOfSameStyle" en "true" para aplicar
// sin espacio entre párrafos con el mismo estilo, lo que agrupará párrafos similares.
// Deje el indicador "NoSpaceBetweenParagraphsOfSameStyle" como "falso"
// para aplicar uniformemente el espaciado a cada párrafo.
builder.ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle = noSpaceBetweenParagraphsOfSameStyle;

builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Quote"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");
builder.Writeln($"Paragraph in the \"{builder.ParagraphFormat.Style.Name}\" style.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingSameStyle.docx");
```

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


