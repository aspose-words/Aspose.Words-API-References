---
title: ListCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Descubra la propiedad Documento ListCollection para acceder fácilmente al documento del propietario y optimizar la gestión de datos. ¡Desbloquee la eficiencia hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.lists/listcollection/document/
---
## ListCollection.Document property

Obtiene el documento del propietario.

```csharp
public DocumentBase Document { get; }
```

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

### Ver también

* class [DocumentBase](../../../aspose.words/documentbase/)
* class [ListCollection](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
