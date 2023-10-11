---
title: ListCollection.Item
second_title: Referencia de API de Aspose.Words para .NET
description: ListCollection propiedad. Obtiene una lista por índice.
type: docs
weight: 30
url: /es/net/aspose.words.lists/listcollection/item/
---
## ListCollection indexer

Obtiene una lista por índice.

```csharp
public List this[int index] { get; }
```

### Ejemplos

Muestra cómo verificar las propiedades del documento del propietario de las listas.

```csharp
Document doc = new Document();

ListCollection lists = doc.Lists;
Assert.AreEqual(doc, lists.Document);

List list = lists.Add(ListTemplate.BulletDefault);
Assert.AreEqual(doc, list.Document);

Console.WriteLine("Current list count: " + lists.Count);
Console.WriteLine("Is the first document list: " + (lists[0].Equals(list)));
Console.WriteLine("ListId: " + list.ListId);
Console.WriteLine("List is the same by ListId: " + (lists.GetListByListId(1).Equals(list)));
```

Muestra cómo aplicar el formato de lista de una lista existente a una colección de párrafos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1");
builder.Writeln("Paragraph 2");
builder.Write("Paragraph 3");

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

doc.Lists.Add(ListTemplate.NumberDefault);
List list = doc.Lists[0];

foreach (Paragraph paragraph in paras.OfType<Paragraph>())
{
    paragraph.ListFormat.List = list;
    paragraph.ListFormat.ListLevelNumber = 2;
}

Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
```

### Ver también

* class [List](../../list/)
* class [ListCollection](../)
* espacio de nombres [Aspose.Words.Lists](../../listcollection/)
* asamblea [Aspose.Words](../../../)


