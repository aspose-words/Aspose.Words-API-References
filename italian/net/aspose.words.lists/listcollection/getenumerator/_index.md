---
title: ListCollection.GetEnumerator
second_title: Aspose.Words per .NET API Reference
description: ListCollection metodo. Ottiene loggetto enumeratore che enumererà gli elenchi nel documento.
type: docs
weight: 60
url: /it/net/aspose.words.lists/listcollection/getenumerator/
---
## ListCollection.GetEnumerator method

Ottiene l'oggetto enumeratore che enumererà gli elenchi nel documento.

```csharp
public IEnumerator<List> GetEnumerator()
```

### Esempi

Mostra come creare un documento con un campione di tutti gli elenchi di un altro documento.

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

### Guarda anche

* class [List](../../list/)
* class [ListCollection](../)
* spazio dei nomi [Aspose.Words.Lists](../../listcollection/)
* assemblea [Aspose.Words](../../../)


