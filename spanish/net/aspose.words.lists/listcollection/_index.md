---
title: Class ListCollection
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Lists.ListCollection clase. Almacena y administra el formato de listas numeradas y con viñetas utilizadas en un documento.
type: docs
weight: 3470
url: /es/net/aspose.words.lists/listcollection/
---
## ListCollection class

Almacena y administra el formato de listas numeradas y con viñetas utilizadas en un documento.

Para obtener más información, visite el[Trabajar con listas](https://docs.aspose.com/words/net/working-with-lists/) artículo de documentación.

```csharp
public class ListCollection : IEnumerable<List>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | Obtiene el recuento de listas numeradas y con viñetas en el documento. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | Obtiene el documento del propietario. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | Obtiene una lista por índice. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(ListTemplate) | Crea una nueva lista basada en una plantilla predefinida y la agrega a la colección de listas en el documento. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(Style) | Crea una nueva lista que hace referencia a un estilo de lista y la agrega a la colección de listas en el documento. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(List) | Crea una nueva lista copiando la lista especificada y agregándola a la colección de listas en el documento. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Obtiene el objeto enumerador que enumerará las listas en el documento. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(int) | Obtiene una lista mediante un identificador de lista. |

### Observaciones

Una lista en un documento de Microsoft Word es un conjunto de propiedades de formato de lista. El formato de las listas se almacena en el`ListCollection` colección por separado de los párrafos de texto.

No creas objetos de esta clase. siempre hay solo uno`ListCollection` objeto por documento y es accesible a través del[`Lists`](../../aspose.words/documentbase/lists/) propiedad.

Para crear una nueva lista basada en una plantilla de lista predefinida o en un estilo de lista, use el[`Add`](./add/) método.

Para crear una nueva lista con formato idéntico a una lista existente, use el[`AddCopy`](./addcopy/) método.

Para hacer un párrafo con viñetas o numerado, debe aplicar el formato de lista a un párrafo asignando un[`List`](../list/)objetar a the [`List`](../listformat/list/) propiedad de[`ListFormat`](../listformat/).

Para eliminar el formato de lista de un párrafo, utilice el[`RemoveNumbers`](../listformat/removenumbers/) Método .

Si sabe un poco sobre WordprocessingML, entonces sabrá que define conceptos separados para "lista" y "definición de lista". Esto corresponde exactamente a cómo se almacena el formato de lista en un documento de Microsoft Word en el nivel bajo. La definición de lista es como un "esquema" y la lista es como una instancia de una definición de lista.

Para simplificar el modelo de programación, Aspose.Words oculta la distinción entre lista y definición list de la misma manera que Microsoft Word oculta esto en su interfaz de usuario. Esto le permite concentrarse más en cómo desea que se vea su documento, en lugar de construir objetos de bajo nivel para satisfacer los requisitos del formato de archivo de Microsoft Word.

No es posible eliminar listas una vez creadas en la versión actual de Aspose.Words. . Esto es similar a Microsoft Word, donde el usuario no tiene control explícito sobre las definiciones de listas.

### Ejemplos

Muestra cómo crear un documento con una muestra de todas las listas de otro documento.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
}
```

Muestra cómo reiniciar la numeración en una lista copiando una lista.

```csharp
Document doc = new Document();

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 // Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" del generador de documentos.
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

Muestra cómo trabajar con niveles de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Una lista nos permite organizar y decorar conjuntos de párrafos con símbolos de prefijo y sangrías.
 // Podemos crear listas anidadas aumentando el nivel de sangría.
 // Podemos comenzar y finalizar una lista utilizando la propiedad "ListFormat" del generador de documentos.
// Cada párrafo que agreguemos entre el inicio y el final de una lista se convertirá en un elemento de la lista.
// A continuación se muestran dos tipos de listas que podemos crear usando un generador de documentos.
// 1 - Una lista numerada:
// Las listas numeradas crean un orden lógico para sus párrafos numerando cada elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Al establecer la propiedad "ListLevelNumber", podemos aumentar el nivel de la lista
// para comenzar una sublista autónoma en el elemento de la lista actual.
// La plantilla de lista de Microsoft Word llamada "NumberDefault" usa números para crear niveles de lista para el primer nivel de lista.
 // Los niveles de lista más profundos utilizan letras y números romanos en minúscula.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Una lista con viñetas:
// Esta lista aplicará una sangría y un símbolo de viñeta ("•") antes de cada párrafo.
// Los niveles más profundos de esta lista utilizarán diferentes símbolos, como "■" y "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Podemos deshabilitar el formato de la lista para no formatear ningún párrafo posterior como lista al desactivar el indicador "Lista".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Ver también

* class [List](../list/)
* espacio de nombres [Aspose.Words.Lists](../../aspose.words.lists/)
* asamblea [Aspose.Words](../../)


