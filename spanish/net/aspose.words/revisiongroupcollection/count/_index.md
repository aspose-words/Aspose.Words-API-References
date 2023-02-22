---
title: RevisionGroupCollection.Count
second_title: Referencia de API de Aspose.Words para .NET
description: RevisionGroupCollection propiedad. Devuelve el número de grupos de revisión de la colección.
type: docs
weight: 10
url: /es/net/aspose.words/revisiongroupcollection/count/
---
## RevisionGroupCollection.Count property

Devuelve el número de grupos de revisión de la colección.

```csharp
public int Count { get; }
```

### Ejemplos

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
* espacio de nombres [Aspose.Words](../../revisiongroupcollection/)
* asamblea [Aspose.Words](../../../)


