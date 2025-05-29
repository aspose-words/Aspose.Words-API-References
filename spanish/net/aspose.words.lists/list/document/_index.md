---
title: List.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Descubra cómo listar las propiedades de los documentos y acceder a la información de propiedad fácilmente. ¡Desbloquee su potencial de gestión documental hoy mismo!
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

Una lista siempre tiene un documento padre y solo es válida en el contexto de ese documento.

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
* class [List](../)
* espacio de nombres [Aspose.Words.Lists](../../../aspose.words.lists/)
* asamblea [Aspose.Words](../../../)
