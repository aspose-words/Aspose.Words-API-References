---
title: ListCollection Class
linktitle: ListCollection
articleTitle: ListCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Lists.ListCollection para una gestión eficiente de listas numeradas y con viñetas, mejorando el formato y la organización de los documentos.
type: docs
weight: 3920
url: /es/net/aspose.words.lists/listcollection/
---
## ListCollection class

Almacena y administra el formato de listas numeradas y con viñetas utilizadas en un documento.

Para obtener más información, visite el[Trabajar con listas](https://docs.aspose.com/words/net/working-with-lists/) Artículo de documentación.

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
| [Add](../../aspose.words.lists/listcollection/add/#add)(*[ListTemplate](../listtemplate/)*) | Crea una nueva lista basada en una plantilla predefinida y la agrega a la colección de listas del documento. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(*[Style](../../aspose.words/style/)*) | Crea una nueva lista que hace referencia a un estilo de lista y la agrega a la colección de listas en el documento. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(*[List](../list/)*) | Crea una nueva lista copiando la lista especificada y agregándola a la colección de listas en el documento. |
| [AddSingleLevelList](../../aspose.words.lists/listcollection/addsinglelevellist/)(*[ListTemplate](../listtemplate/)*) | Crea una nueva lista de un solo nivel basada en la plantilla predefinida y la agrega a la colección de listas en el documento. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Obtiene el objeto enumerador que enumerará las listas en el documento. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(*int*) | Obtiene una lista mediante un identificador de lista. |

## Observaciones

Una lista en un documento de Microsoft Word es un conjunto de propiedades de formato de lista. El formato de las listas se almacena en el`ListCollection` colección por separado de los párrafos de texto.

No se crean objetos de esta clase. Siempre hay uno solo.`ListCollection` objeto por documento y es accesible a través de[`Lists`](../../aspose.words/documentbase/lists/) propiedad.

Para crear una nueva lista basada en una plantilla de lista predefinida o basada en un estilo de lista, utilice el comando[`Add`](./add/) método.

Para crear una nueva lista con un formato idéntico a una lista existente, utilice el comando [`AddCopy`](./addcopy/) método.

Para hacer que un párrafo tenga viñetas o numeración, debe aplicar el formato de lista a un párrafo asignando un[`List`](../list/)objeto al [`List`](../listformat/list/) propiedad de[`ListFormat`](../listformat/).

Para eliminar el formato de lista de un párrafo, utilice el[`RemoveNumbers`](../listformat/removenumbers/) Método .

Si conoces WordprocessingML, probablemente sepas que define conceptos separados para "lista" y "definición de lista". Esto se corresponde exactamente con cómo se almacena el formato de lista en un documento de Microsoft Word a bajo nivel. La definición de lista es como un "esquema" y la lista es como una instancia de una definición de lista.

Para simplificar el modelo de programación, Aspose.Words oculta la distinción entre lista y definición de lista de la misma manera que Microsoft Word la oculta en su interfaz de usuario. Esto le permite concentrarse más en cómo quiere que se vea su documento, en lugar de construir objetos de bajo nivel para satisfacer los requisitos del formato de archivo de Microsoft Word.

No es posible eliminar listas una vez creadas en la versión actual de Aspose.Words. . Esto es similar a Microsoft Word, donde el usuario no tiene control explícito sobre las definiciones de listas.

## Ejemplos

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

* class [List](../list/)
* espacio de nombres [Aspose.Words.Lists](../../aspose.words.lists/)
* asamblea [Aspose.Words](../../)
