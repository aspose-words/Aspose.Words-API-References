---
title: List Class
linktitle: List
articleTitle: List
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Lists.List para un formato de listas potente. Mejore sus documentos con una organización impecable y una presentación profesional.
type: docs
weight: 3910
url: /es/net/aspose.words.lists/list/
---
## List class

Representa el formato de una lista.

Para obtener más información, visite el[Trabajar con listas](https://docs.aspose.com/words/net/working-with-lists/) Artículo de documentación.

```csharp
public class List : IComparable<List>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Obtiene el documento del propietario. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Devuelve`verdadero` si esta lista es una definición de un estilo de lista. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Devuelve`verdadero` si esta lista es una referencia a un estilo de lista. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Devuelve`verdadero` cuando la lista contiene 9 niveles;`FALSO` cuando 1 nivel. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Especifica si la lista debe reiniciarse en cada sección. El valor predeterminado es`FALSO` . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Obtiene el identificador único de la lista. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Obtiene la colección de niveles de lista para esta lista. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Obtiene el estilo de lista al que esta lista hace referencia o define. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(*List*) | Compara la lista especificada con la lista actual. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(*object*) | Compara el objeto especificado con el objeto actual. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(*List*) | Compara con la lista especificada. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(*object*) | Determina si el objeto especificado es igual en valor al objeto actual. |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Calcula el código hash para este objeto de lista. |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(*List*) | Devuelve verdadero si la lista actual y la lista dada se crean a partir de la misma plantilla. |

## Observaciones

Una lista en un documento de Microsoft Word es un conjunto de propiedades de formato de lista. Cada lista puede tener hasta 9 niveles y las propiedades de formato, como el estilo de número, el valor inicial, la sangría, la posición de tabulación, etc., se definen por separado para cada nivel.

A`List` El objeto siempre pertenece al[`ListCollection`](../listcollection/) recopilación.

Para crear una nueva lista, utilice los métodos Agregar del[`ListCollection`](../listcollection/) recopilación.

Para modificar el formato de una lista, utilice[`ListLevel`](../listlevel/) objetos encontrados en el[`ListLevels`](./listlevels/) recopilación.

Para aplicar o eliminar el formato de lista de un párrafo, utilice[`ListFormat`](../listformat/).

## Ejemplos

Muestra cómo reiniciar la numeración en una lista copiando una lista.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// Cree una lista a partir de una plantilla de Microsoft Word y personalice su primer nivel de lista.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

//Aplica nuestra lista a algunos párrafos.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

//Podemos agregar una copia de una lista existente a la colección de listas del documento
// para crear una lista similar sin realizar cambios en la original.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Aplicar la segunda lista a los nuevos párrafos.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

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

Muestra cómo trabajar con niveles de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 //Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" de un generador de documentos.
//Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
//A continuación se muestran dos tipos de listas que podemos crear usando un generador de documentos.
// 1 - Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
// para comenzar una sublista autónoma en el elemento de lista actual.
// La plantilla de lista de Microsoft Word llamada "NumberDefault" utiliza números para crear niveles de lista para el primer nivel de lista.
 // Los niveles de lista más profundos utilizan letras y números romanos en minúscula.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Una lista con viñetas:
//Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
// Los niveles más profundos de esta lista utilizarán símbolos diferentes, como "■" y "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Podemos deshabilitar el formato de lista para no formatear los párrafos subsiguientes como listas desmarcando la marca "Lista".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Ver también

* espacio de nombres [Aspose.Words.Lists](../../aspose.words.lists/)
* asamblea [Aspose.Words](../../)
