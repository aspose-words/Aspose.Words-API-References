---
title: ParagraphFormat.SpaceAfter
linktitle: SpaceAfter
articleTitle: SpaceAfter
second_title: Aspose.Words para .NET
description: Controle el espaciado entre párrafos con la propiedad SpaceAfter. Ajuste fácilmente el espaciado en puntos para mejorar la legibilidad y la presentación de su documento.
type: docs
weight: 310
url: /es/net/aspose.words/paragraphformat/spaceafter/
---
## ParagraphFormat.SpaceAfter property

Obtiene o establece la cantidad de espacio (en puntos) después del párrafo.

```csharp
public double SpaceAfter { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza cuando el argumento está fuera del rango de valores válidos. |

## Observaciones

No tiene efecto cuando[`SpaceAfterAuto`](../spaceafterauto/) es`verdadero`.

Los valores válidos oscilan entre 0 y 1584 inclusive.

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
