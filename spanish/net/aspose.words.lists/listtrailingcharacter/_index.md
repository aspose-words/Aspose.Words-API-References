---
title: ListTrailingCharacter Enum
linktitle: ListTrailingCharacter
articleTitle: ListTrailingCharacter
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Lists.ListTrailingCharacter para personalizar las etiquetas de lista y mejorar el formato de párrafo para una presentación pulida del documento.
type: docs
weight: 3990
url: /es/net/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enumeration

Especifica el carácter que separa la etiqueta de la lista del texto del párrafo.

```csharp
public enum ListTrailingCharacter
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Tab | `0` | Se coloca un carácter de tabulación entre la etiqueta de la lista y el texto del párrafo. |
| Space | `1` | Se coloca un carácter de espacio entre la etiqueta de la lista y el texto del párrafo. |
| Nothing | `2` | No hay ningún carácter separador entre la etiqueta de la lista y el texto del párrafo. |

## Observaciones

Se utiliza como valor para el[`TrailingCharacter`](../listlevel/trailingcharacter/) propiedad.

## Ejemplos

Muestra cómo aplicar formato de lista personalizado a los párrafos cuando se utiliza DocumentBuilder.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice los dos primeros niveles de lista.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Este valor de NumberFormat creará símbolos de lista con viñetas en forma de estrella.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Cree párrafos y aplíqueles ambos niveles de lista de nuestro formato de lista personalizado.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Lists](../../aspose.words.lists/)
* asamblea [Aspose.Words](../../)
