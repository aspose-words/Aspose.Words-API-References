---
title: ListCollection.AddCopy
linktitle: AddCopy
articleTitle: AddCopy
second_title: Aspose.Words para .NET
description: Descubra el método AddCopy de ListCollection para duplicar una lista sin esfuerzo y mejorar la colección de sus documentos con facilidad y eficiencia.
type: docs
weight: 50
url: /es/net/aspose.words.lists/listcollection/addcopy/
---
## ListCollection.AddCopy method

Crea una nueva lista copiando la lista especificada y agregándola a la colección de listas en el documento.

```csharp
public List AddCopy(List srcList)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| srcList | List | La lista de fuentes desde donde copiar. |

### Valor_devuelto

La lista recién creada.

## Observaciones

La lista de origen puede provenir de cualquier documento. Si pertenece a otro documento, se crea una copia y se agrega al documento actual.

Si la lista de origen es una referencia o una definición de un estilo de lista, la lista recién creada no está relacionada con el estilo de lista original.

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

### Ver también

* class [List](../../list/)
* class [ListCollection](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
