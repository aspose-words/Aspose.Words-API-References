---
title: ParagraphFormat.SpaceBeforeAuto
linktitle: SpaceBeforeAuto
articleTitle: SpaceBeforeAuto
second_title: Aspose.Words para .NET
description: Descubra la propiedad ParagraphFormat SpaceBeforeAuto. Ajuste automáticamente el espaciado entre párrafos para lograr un aspecto profesional y elegante en sus documentos.
type: docs
weight: 340
url: /es/net/aspose.words/paragraphformat/spacebeforeauto/
---
## ParagraphFormat.SpaceBeforeAuto property

Verdadero si la cantidad de espacio antes del párrafo se establece automáticamente.

```csharp
public bool SpaceBeforeAuto { get; set; }
```

## Observaciones

Cuando se establece en`verdadero` , anula el efecto de[`SpaceBefore`](../spacebefore/).

Cuando configura el Espacio antes y el Espacio después del párrafo en Automático, Microsoft Word agrega 14 puntos de espacio entre párrafos automáticamente de acuerdo con las siguientes reglas:

* Normalmente, se agrega espaciado después de todos los párrafos.
* En una lista numerada o con viñetas, el espaciado se agrega solo después del último elemento de la lista. No se agrega espaciado entre los elementos de la lista.
* En una lista numerada o con viñetas anidadas no se agrega espaciado.
* El espaciado normalmente se agrega después de una tabla.
* No se agrega espaciado después de una tabla si es el último bloque en una celda de la tabla.
* No se agrega espaciado después del último párrafo en una celda de tabla.

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

### Ver también

* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
