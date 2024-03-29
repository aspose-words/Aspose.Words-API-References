---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words para .NET
description: ParagraphFormat NoSpaceBetweenParagraphsOfSameStyle propiedad. cuandoverdadero SpaceBefore ySpaceAfter será ignorado entre los párrafos del mismo estilo en C#.
type: docs
weight: 240
url: /es/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

cuando`verdadero` ,[`SpaceBefore`](../spacebefore/) y[`SpaceAfter`](../spaceafter/) será ignorado entre los párrafos del mismo estilo.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## Observaciones

Esta configuración solo tiene efecto cuando se aplica a un estilo de párrafo. Si se aplica a un párrafo directamente, no tiene ningún efecto.

## Ejemplos

Muestra cómo no aplicar espacios entre párrafos con el mismo estilo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aplique una gran cantidad de espacio antes y después de los párrafos que creará este constructor.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Establece el indicador "NoSpaceBetweenParagraphsOfSameStyle" en "true" para aplicar
// sin espacios entre párrafos con el mismo estilo, lo que agrupará párrafos similares.
// Deja el indicador "NoSpaceBetweenParagraphsOfSameStyle" como "falso"
// para aplicar espaciado uniformemente a cada párrafo.
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
