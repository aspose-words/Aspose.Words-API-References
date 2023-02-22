---
title: ParagraphFormat.SpaceBeforeAuto
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Verdadero si la cantidad de espacio antes del párrafo se establece automáticamente.
type: docs
weight: 320
url: /es/net/aspose.words/paragraphformat/spacebeforeauto/
---
## ParagraphFormat.SpaceBeforeAuto property

Verdadero si la cantidad de espacio antes del párrafo se establece automáticamente.

```csharp
public bool SpaceBeforeAuto { get; set; }
```

### Observaciones

Cuando se establece en verdadero, anula el efecto de[`SpaceBefore`](../spacebefore/).

Cuando configura el espacio anterior y posterior del párrafo en Auto, Microsoft Word agrega 14 puntos de espaciado entre párrafos automáticamente de acuerdo con las siguientes reglas:

* Normalmente, el espaciado se agrega después de todos los párrafos.
* En una lista numerada o con viñetas, el espacio se agrega solo después del último elemento de la lista. El espacio no se agrega entre los elementos de la lista.
* En una lista anidada con viñetas o numerada, no se agrega espacio.
* El espaciado normalmente se agrega después de una tabla.
* El espaciado no se agrega después de una tabla si es el último bloque en una celda de la tabla.
* El espacio no se agrega después del último párrafo en una celda de tabla.

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

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


