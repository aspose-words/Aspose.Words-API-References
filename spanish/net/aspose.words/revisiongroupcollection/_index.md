---
title: RevisionGroupCollection Class
linktitle: RevisionGroupCollection
articleTitle: RevisionGroupCollection
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.RevisionGroupCollection, que ofrece una gestión eficiente de grupos de revisión de documentos para mejorar la edición y la colaboración.
type: docs
weight: 5530
url: /es/net/aspose.words/revisiongroupcollection/
---
## RevisionGroupCollection class

Una colección de[`RevisionGroup`](../revisiongroup/)objetos que representan grupos de revisión en el documento.

Para obtener más información, visite el[Seguimiento de cambios en un documento](https://docs.aspose.com/words/net/track-changes-in-a-document/) Artículo de documentación.

```csharp
public sealed class RevisionGroupCollection : IEnumerable<RevisionGroup>
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Count](../../aspose.words/revisiongroupcollection/count/) { get; } | Devuelve el número de grupos de revisión en la colección. |
| [Item](../../aspose.words/revisiongroupcollection/item/) { get; } | Devuelve un grupo de revisión en el índice especificado. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words/revisiongroupcollection/getenumerator/)() | Devuelve un objeto enumerador. |

## Observaciones

No se crean instancias de esta clase directamente. Utilice el[`Groups`](../revisioncollection/groups/) Propiedad para obtener los grupos de revisión presentes en un documento.

## Ejemplos

Muestra cómo obtener un grupo de revisiones en un documento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

RevisionGroup revisionGroup = doc.Revisions.Groups[0];
```

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

* class [RevisionGroup](../revisiongroup/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
