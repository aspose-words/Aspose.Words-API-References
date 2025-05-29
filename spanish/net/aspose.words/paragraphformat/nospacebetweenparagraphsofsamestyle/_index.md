---
title: ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle
linktitle: NoSpaceBetweenParagraphsOfSameStyle
articleTitle: NoSpaceBetweenParagraphsOfSameStyle
second_title: Aspose.Words para .NET
description: Descubra la propiedad NoSpaceBetweenParagraphsOfSameStyle de ParagraphFormat. Optimice el diseño de su documento eliminando el espacio entre párrafos del mismo estilo.
type: docs
weight: 250
url: /es/net/aspose.words/paragraphformat/nospacebetweenparagraphsofsamestyle/
---
## ParagraphFormat.NoSpaceBetweenParagraphsOfSameStyle property

Cuando`verdadero` ,[`SpaceBefore`](../spacebefore/) y[`SpaceAfter`](../spaceafter/) Se ignorará entre los párrafos del mismo estilo.

```csharp
public bool NoSpaceBetweenParagraphsOfSameStyle { get; set; }
```

## Observaciones

Esta configuración solo tiene efecto al aplicarse a un estilo de párrafo. Si se aplica directamente a un párrafo, no tiene efecto.

## Ejemplos

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
