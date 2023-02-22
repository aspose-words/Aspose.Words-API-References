---
title: ListCollection.GetListByListId
second_title: Referencia de API de Aspose.Words para .NET
description: ListCollection método. Obtiene una lista por un identificador de lista.
type: docs
weight: 70
url: /es/net/aspose.words.lists/listcollection/getlistbylistid/
---
## ListCollection.GetListByListId method

Obtiene una lista por un identificador de lista.

```csharp
public List GetListByListId(int listId)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| listId | Int32 | El identificador de la lista. |

### Valor_devuelto

Devuelve el objeto de la lista. Devuelve nulo si no se encuentra una lista con el identificador especificado.

### Observaciones

Normalmente no es necesario utilizar este método. La mayoría de las veces aplica el formato de lista a los párrafos simplemente configurando el[`List`](../../listformat/list/) propiedad de la[`ListFormat`](../../listformat/) objeto.

### Ejemplos

Muestra cómo verificar las propiedades del documento de propietario de las listas.

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

* class [List](../../list/)
* class [ListCollection](../)
* espacio de nombres [Aspose.Words.Lists](../../listcollection/)
* asamblea [Aspose.Words](../../../)


