---
title: RevisionGroupCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words para .NET
description: Descubra la propiedad Count de RevisionGroupCollection. Recupera fácilmente el número total de grupos de revisión, optimizando la gestión de datos.
type: docs
weight: 10
url: /es/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Devuelve el número de grupos de revisión en la colección.

```csharp
public int Count { get; }
```

## Ejemplos

Muestra cómo imprimir información sobre un grupo de revisiones en un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Assert.AreEqual(7, doc.Revisions.Groups.Count);

foreach (RevisionGroup group in doc.Revisions.Groups)
{
    Console.WriteLine(
        $"Revision author: {group.Author}; Revision type: {group.RevisionType} \n\tRevision text: {group.Text}");
}
```

### Ver también

* class [RevisionGroupCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
