---
title: Enum DropCapPosition
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.DropCapPosition enumeración. Especifica la posición de un texto capitular.
type: docs
weight: 1260
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
| None | `0` | El párrafo no tiene capitular. |
| Normal | `1` | La letra capitular se coloca dentro del margen de texto en el párrafo ancla. |
| Margin | `2` | La letra capitular se coloca fuera del margen de texto en el párrafo ancla. |

### Ejemplos

Muestra cómo crear una letra capitular.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserta un párrafo con una letra grande con la que comienza el texto en el segundo y tercer párrafo.
builder.Font.Size = 54;
builder.Writeln("L");

builder.Font.Size = 18;
builder.Writeln("orem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
builder.Writeln("Ut enim ad minim veniam, quis nostrud exercitation " +
                "ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Actualmente, el segundo y tercer párrafo aparecerán debajo del primero.
// Podemos convertir el primer párrafo como capitular para los otros párrafos a través de su objeto "ParagraphFormat".
// Establecer la propiedad "DropCapPosition" en "DropCapPosition.Margin" para colocar la letra capitular
// fuera del margen de la página del lado izquierdo si nuestro texto es de izquierda a derecha.
// Establecer la propiedad "DropCapPosition" en "DropCapPosition.Normal" para colocar la letra capitular dentro de los márgenes de la página
// y para envolver el resto del texto a su alrededor.
// "DropCapPosition.None" es el estado predeterminado para todos los párrafos.
ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.DropCapPosition = dropCapPosition;

doc.Save(ArtifactsDir + "ParagraphFormat.DropCap.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


