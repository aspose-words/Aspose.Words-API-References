---
title: ParagraphFormat.SpaceBefore
linktitle: SpaceBefore
articleTitle: SpaceBefore
second_title: Aspose.Words para .NET
description: Descubra la propiedad ParagraphFormat SpaceBefore para ajustar fácilmente el espaciado de párrafo en puntos, mejorando la legibilidad y el estilo de su documento.
type: docs
weight: 330
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
| ArgumentOutOfRangeException | Se lanza cuando el argumento está fuera del rango de valores válidos. |

## Observaciones

No tiene efecto cuando[`SpaceBeforeAuto`](../spacebeforeauto/) es`verdadero`.

Los valores válidos varían de 0 a 1584 inclusive.

## Ejemplos

Muestra cómo configurar el espaciado automático de párrafos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aplique una gran cantidad de espaciado antes y después de los párrafos que creará este constructor.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Establezca estos indicadores en "verdadero" para aplicar el espaciado automático,
// ignorando efectivamente el espaciado en las propiedades que establecimos arriba.
// Déjelos como "falso" y se aplicará nuestro espaciado de párrafo personalizado.
builder.ParagraphFormat.SpaceAfterAuto = autoSpacing;
builder.ParagraphFormat.SpaceBeforeAuto = autoSpacing;

// Inserte dos párrafos que tendrán espacio arriba y abajo de ellos y guarde el documento.
builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphSpacingAuto.docx");
```

Muestra cómo no aplicar espacio entre párrafos con el mismo estilo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aplique una gran cantidad de espaciado antes y después de los párrafos que creará este constructor.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Establezca el indicador "NoSpaceBetweenParagraphsOfSameStyle" en "verdadero" para aplicar
// sin espacio entre párrafos con el mismo estilo, lo que agrupará párrafos similares.
// Deje el indicador "NoSpaceBetweenParagraphsOfSameStyle" como "falso"
// para aplicar el espaciado uniformemente a cada párrafo.
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
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
