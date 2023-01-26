---
title: List
second_title: Referencia de API de Aspose.Words para .NET
description: Representa el formato de una lista.
type: docs
weight: 3260
url: /es/net/aspose.words.lists/list/
---
## List class

Representa el formato de una lista.

```csharp
public class List : IComparable<List>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Obtiene el documento del propietario. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Devuelve verdadero si esta lista es una definición de un estilo de lista. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Devuelve verdadero si esta lista es una referencia a un estilo de lista. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Devuelve verdadero cuando la lista contiene 9 niveles; falso cuando 1 nivel. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Especifica si la lista debe reiniciarse en cada sección. El valor predeterminado es **falso** . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Obtiene el identificador único de la lista. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Obtiene la colección de niveles de lista para esta lista. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Obtiene el estilo de lista al que hace referencia o define esta lista. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(List) | Compara la lista especificada con la lista actual. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(object) | Compara el objeto especificado con el objeto actual. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(List) | Compara con la lista especificada. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(object) |  |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Calcula el código hash para este objeto de lista. |

### Observaciones

Una lista en un documento de Microsoft Word es un conjunto de propiedades de formato de lista. Cada lista puede tener hasta 9 niveles y las propiedades de formato, como estilo de número, valor inicial, sangría, posición de tabulación, etc., se definen por separado para cada nivel.

A`List` objeto siempre pertenece a la[`ListCollection`](../listcollection/) recopilación.

Para crear una nueva lista, use los métodos Agregar del[`ListCollection`](../listcollection/) recopilación.

Para modificar el formato de una lista, utilice[`ListLevel`](../listlevel/) objetos encontrados en el[`ListLevels`](./listlevels/) recopilación.

Para aplicar o eliminar el formato de lista de un párrafo, use[`ListFormat`](../listformat/).

### Ejemplos

Muestra cómo reiniciar la numeración en una lista copiando una lista.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría. 
// Podemos comenzar y finalizar una lista usando la propiedad "ListFormat" del generador de documentos. 
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice su primer nivel de lista.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Aplicar nuestra lista a algunos párrafos.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Podemos agregar una copia de una lista existente a la colección de listas del documento
// para crear una lista similar sin realizar cambios en la original.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Aplicar la segunda lista a nuevos párrafos.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

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

Muestra cómo trabajar con niveles de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
// Podemos crear listas anidadas aumentando el nivel de sangría. 
// Podemos comenzar y finalizar una lista usando la propiedad "ListFormat" del generador de documentos. 
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// A continuación hay dos tipos de listas que podemos crear usando un generador de documentos.
// 1 - Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
// para comenzar una sublista independiente en el elemento de la lista actual.
// La plantilla de lista de Microsoft Word llamada "NumberDefault" usa números para crear niveles de lista para el primer nivel de lista.
// Los niveles de lista más profundos usan letras y números romanos en minúsculas. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Una lista con viñetas:
// Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
// Los niveles más profundos de esta lista usarán diferentes símbolos, como "■" y "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Podemos deshabilitar el formato de la lista para no formatear los párrafos posteriores como listas al deshabilitar el indicador "Lista".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Lists](../../aspose.words.lists/)
* asamblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
