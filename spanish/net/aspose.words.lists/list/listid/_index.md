---
title: List.ListId
linktitle: ListId
articleTitle: ListId
second_title: Aspose.Words para .NET
description: Descubre la propiedad única ListId para acceder y gestionar fácilmente tus listas. Optimiza tu flujo de trabajo con este identificador esencial.
type: docs
weight: 60
url: /es/net/aspose.words.lists/list/listid/
---
## List.ListId property

Obtiene el identificador único de la lista.

```csharp
public int ListId { get; }
```

## Observaciones

Normalmente no es necesario usar esta propiedad. Pero si la usa, normalmente lo hace junto con la propiedad so .[`GetListByListId`](../../listcollection/getlistbylistid/) método para encontrar una lista por su identificador.

## Ejemplos

Muestra cómo verificar las propiedades del documento propietario de las listas.

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

Muestra cómo generar todos los párrafos de un documento que son elementos de lista.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Bulleted list item 1");
builder.Writeln("Bulleted list item 2");
builder.Writeln("Bulleted list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

foreach (Paragraph para in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{ 
    Console.WriteLine($"This paragraph belongs to list ID# {para.ListFormat.List.ListId}, number style \"{para.ListFormat.ListLevel.NumberStyle}\"");
    Console.WriteLine($"\t\"{para.GetText().Trim()}\"");
}
```

### Ver también

* class [List](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
