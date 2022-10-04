---
title: ListLevel
second_title: Referencia de API de Aspose.Words para .NET
description: Define el formato para un nivel de lista.
type: docs
weight: 3300
url: /es/net/aspose.words.lists/listlevel/
---
## ListLevel class

Define el formato para un nivel de lista.

```csharp
public class ListLevel
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Alignment](../../aspose.words.lists/listlevel/alignment/) { get; set; } | Obtiene o establece la justificación del número real del elemento de la lista. |
| [CustomNumberStyleFormat](../../aspose.words.lists/listlevel/customnumberstyleformat/) { get; } | Obtiene el formato de estilo de número personalizado para este nivel de lista. Por ejemplo: "a, ç, ĝ, ...". |
| [Font](../../aspose.words.lists/listlevel/font/) { get; } | Especifica el formato de caracteres utilizado para la etiqueta de la lista. |
| [ImageData](../../aspose.words.lists/listlevel/imagedata/) { get; } | Devuelve datos de imagen de la forma de viñeta de imagen para el nivel de lista actual. |
| [IsLegal](../../aspose.words.lists/listlevel/islegal/) { get; set; } | Verdadero si el nivel convierte todos los números heredados a árabe, falso si conserva su estilo numérico. |
| [LinkedStyle](../../aspose.words.lists/listlevel/linkedstyle/) { get; set; } | Obtiene o establece el estilo de párrafo que está vinculado a este nivel de lista. |
| [NumberFormat](../../aspose.words.lists/listlevel/numberformat/) { get; set; } | Devuelve o establece el formato de número para el nivel de lista. |
| [NumberPosition](../../aspose.words.lists/listlevel/numberposition/) { get; set; } | Devuelve o establece la posición (en puntos) del número o viñeta para el nivel de lista. |
| [NumberStyle](../../aspose.words.lists/listlevel/numberstyle/) { get; set; } | Devuelve o establece el estilo de número para este nivel de lista. |
| [RestartAfterLevel](../../aspose.words.lists/listlevel/restartafterlevel/) { get; set; } | Establece o devuelve el nivel de lista que debe aparecer antes de que el nivel de lista especificado reinicie la numeración. |
| [StartAt](../../aspose.words.lists/listlevel/startat/) { get; set; } | Devuelve o establece el número inicial para este nivel de lista. |
| [TabPosition](../../aspose.words.lists/listlevel/tabposition/) { get; set; } | Devuelve o establece la posición de tabulación (en puntos) para el nivel de lista. |
| [TextPosition](../../aspose.words.lists/listlevel/textposition/) { get; set; } | Devuelve o establece la posición (en puntos) de la segunda línea de texto envolvente para el nivel de lista. |
| [TrailingCharacter](../../aspose.words.lists/listlevel/trailingcharacter/) { get; set; } | Devuelve o establece el carácter insertado después del número para el nivel de lista. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [CreatePictureBullet](../../aspose.words.lists/listlevel/createpicturebullet/)() | Crea una forma de viñeta de imagen para el nivel de lista actual. |
| [DeletePictureBullet](../../aspose.words.lists/listlevel/deletepicturebullet/)() | Elimina la viñeta de imagen para el nivel de lista actual. |
| [Equals](../../aspose.words.lists/listlevel/equals/#equals)(ListLevel) | Compara con el ListLevel especificado. |
| override [GetHashCode](../../aspose.words.lists/listlevel/gethashcode/)() | Calcula el código hash para este objeto. |
| static [GetEffectiveValue](../../aspose.words.lists/listlevel/geteffectivevalue/)(int, NumberStyle, string) | Reporta la representación de cadena del[`ListLevel`](./listlevel/) objeto para el índice especificado del elemento de la lista. Los parámetros especifican el[`NumberStyle`](../../aspose.words/numberstyle/) y un formato opcional string utilizado cuandoCustom se especifica. |

### Observaciones

No creas objetos de esta clase. Los objetos de nivel de lista se crean automáticamente cuando se crea una lista. accedes[`ListLevel`](./listlevel/) objetos a través de the [`ListLevelCollection`](../listlevelcollection/) recopilación.

Usa las propiedades de[`ListLevel`](./listlevel/) para especificar el formato de lista para niveles de lista individuales.

### Ejemplos

Muestra cómo aplicar un formato de lista personalizado a los párrafos cuando se usa DocumentBuilder.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría. 
// Podemos comenzar y finalizar una lista usando la propiedad "ListFormat" del generador de documentos. 
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice los dos primeros niveles de la lista.
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

// Este valor de NumberFormat creará símbolos de lista de viñetas en forma de estrella.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Crear párrafos y aplicarles ambos niveles de lista de nuestro formato de lista personalizado.
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

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
