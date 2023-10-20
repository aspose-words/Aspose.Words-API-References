---
title: DropCapPosition Enum
linktitle: DropCapPosition
articleTitle: DropCapPosition
second_title: Aspose.Words para .NET
description: Aspose.Words.DropCapPosition enumeración. Especifica la posición de un texto capitular en C#.
type: docs
weight: 1410
url: /es/net/aspose.words/dropcapposition/
---
## DropCapPosition enumeration

Especifica la posición de un texto capitular.

```csharp
public enum DropCapPosition
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | El párrafo no tiene letra capitular. |
| Normal | `1` | La letra capitular se coloca dentro del margen del texto en el párrafo de anclaje. |
| Margin | `2` | La letra capitular se coloca fuera del margen del texto en el párrafo de anclaje. |

## Ejemplos

Muestra cómo crear una letra capitular.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserte un párrafo con una letra grande con la que comienza el texto del segundo y tercer párrafo.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Actualmente, el segundo y tercer párrafo aparecerán debajo del primero.
// Podemos convertir el primer párrafo como un capitular para los otros párrafos a través de su objeto "ParagraphFormat".
// Establece la propiedad "DropCapPosition" en "DropCapPosition.Margin" para colocar la letra capital
// fuera del margen izquierdo de la página si nuestro texto es de izquierda a derecha.
// Establece la propiedad "DropCapPosition" en "DropCapPosition.Normal" para colocar la letra capitular dentro de los márgenes de la página
// y envolver el resto del texto a su alrededor.
// "DropCapPosition.None" es el estado predeterminado para todos los párrafos.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
