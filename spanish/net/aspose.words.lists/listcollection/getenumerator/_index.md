---
title: ListCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words para .NET
description: ListCollection GetEnumerator método. Obtiene el objeto enumerador que enumerará las listas en el documento en C#.
type: docs
weight: 60
url: /es/net/aspose.words.lists/listcollection/getenumerator/
---
## ListCollection.GetEnumerator method

Obtiene el objeto enumerador que enumerará las listas en el documento.

```csharp
public IEnumerator<List> GetEnumerator()
```

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

### Ver también

* class [List](../../list/)
* class [ListCollection](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
