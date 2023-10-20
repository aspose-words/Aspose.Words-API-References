---
title: ListCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words för .NET
description: ListCollection GetEnumerator metod. Hämtar uppräkningsobjektet som kommer att räkna upp listor i dokumentet i C#.
type: docs
weight: 60
url: /sv/net/aspose.words.lists/listcollection/getenumerator/
---
## ListCollection.GetEnumerator method

Hämtar uppräkningsobjektet som kommer att räkna upp listor i dokumentet.

```csharp
public IEnumerator<List> GetEnumerator()
```

## Exempel

Visar hur man skapar ett dokument med ett exempel på alla listor från ett annat dokument.

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

### Se även

* class [List](../../list/)
* class [ListCollection](../)
* namnutrymme [Aspose.Words.Lists](../../../aspose.words.lists/)
* hopsättning [Aspose.Words](../../../)
