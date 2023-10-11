---
title: ParagraphFormat.SpaceAfterAuto
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Verdadero si la cantidad de espacio después del párrafo se establece automáticamente.
type: docs
weight: 310
url: /es/net/aspose.words/paragraphformat/spaceafterauto/
---
## ParagraphFormat.SpaceAfterAuto property

Verdadero si la cantidad de espacio después del párrafo se establece automáticamente.

```csharp
public bool SpaceAfterAuto { get; set; }
```

### Observaciones

Cuando se establece en`verdadero` , anula el efecto de[`SpaceAfter`](../spaceafter/).

Cuando configura el Espacio antes y el Espacio después del párrafo en Automático, Microsoft Word agrega un espacio de 14 puntos entre párrafos automáticamente de acuerdo con las siguientes reglas:

* Normalmente, se agrega espacio después de todos los párrafos.
* En una lista con viñetas o numerada, el espacio se agrega solo después del último elemento de la lista. No se agrega espacio entre los elementos de la lista.
* En una lista anidada con viñetas o numerada no se agrega espacio.
* Normalmente el espacio se añade después de una tabla.
* No se agrega espacio después de una tabla si es el último bloque de una celda de la tabla.
* No se agrega espacio después del último párrafo en una celda de la tabla.

### Ejemplos

Muestra cómo configurar el espaciado automático de párrafos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aplique una gran cantidad de espacio antes y después de los párrafos que creará este constructor.
builder.ParagraphFormat.SpaceBefore = 24;
builder.ParagraphFormat.SpaceAfter = 24;

// Establece estos indicadores en "verdadero" para aplicar el espaciado automático,
// ignorando efectivamente el espaciado en las propiedades que configuramos anteriormente.
// Déjalos como "falso" y se aplicará nuestro espaciado de párrafo personalizado.
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


