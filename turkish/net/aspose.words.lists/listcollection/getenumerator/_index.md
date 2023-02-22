---
title: ListCollection.GetEnumerator
second_title: Aspose.Words for .NET API Referansı
description: ListCollection yöntem. Belgedeki listeleri numaralandıracak numaralandırıcı nesnesini alır.
type: docs
weight: 60
url: /tr/net/aspose.words.lists/listcollection/getenumerator/
---
## ListCollection.GetEnumerator method

Belgedeki listeleri numaralandıracak numaralandırıcı nesnesini alır.

```csharp
public IEnumerator<List> GetEnumerator()
```

### Örnekler

Başka bir belgedeki tüm listelerin bir örneğini içeren bir belgenin nasıl oluşturulacağını gösterir.

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

### Ayrıca bakınız

* class [List](../../list/)
* class [ListCollection](../)
* ad alanı [Aspose.Words.Lists](../../listcollection/)
* toplantı [Aspose.Words](../../../)


