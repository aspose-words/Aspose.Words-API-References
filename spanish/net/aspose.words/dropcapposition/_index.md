---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.DropCapPosition para mejorar el diseño de su documento definiendo posiciones de texto de letra capital únicas para lograr un atractivo visual impactante.
type: docs
weight: 1820
url: /es/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Especifica la posición de un texto de letra capital.

```csharp
public enum DropCapPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El párrafo no tiene letra capital. |
| Normal | `1` | La letra capital se coloca dentro del margen de texto en el párrafo de anclaje. |
| Margin | `2` | La letra capital se coloca fuera del margen de texto en el párrafo de anclaje. |

## Ejemplos

Muestra cómo crear una letra capital.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un párrafo con una letra grande con la que comienza el texto en el segundo y tercer párrafo.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Actualmente, el segundo y tercer párrafo aparecerán debajo del primero.
// Podemos convertir el primer párrafo en una letra capital para los demás párrafos a través de su objeto "ParagraphFormat".
// Establezca la propiedad "DropCapPosition" en "DropCapPosition.Margin" para colocar la letra capital
// fuera del margen izquierdo de la página si nuestro texto es de izquierda a derecha.
// Establezca la propiedad "DropCapPosition" en "DropCapPosition.Normal" para colocar la letra capital dentro de los márgenes de la página
// y envolver el resto del texto a su alrededor.
// "DropCapPosition.None" es el estado predeterminado para todos los párrafos.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
