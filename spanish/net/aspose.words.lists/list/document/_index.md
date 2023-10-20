---
title: List.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: List Document propiedad. Obtiene el documento del propietario en C#.
type: docs
weight: 10
url: /es/net/aspose.words.lists/list/document/
---
## List.Document property

Obtiene el documento del propietario.

```csharp
public DocumentBase Document { get; }
```

## Observaciones

Una lista siempre tiene un documento principal y solo es válida en el contexto de ese documento.

## Ejemplos

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

### Ver también

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [List](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
