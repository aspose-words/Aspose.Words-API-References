---
title: RevisionGroup Class
linktitle: RevisionGroup
articleTitle: RevisionGroup
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.RevisionGroup, diseñada para administrar y organizar de manera eficiente objetos de revisión secuenciales para una edición optimizada de documentos.
type: docs
weight: 5520
url: /es/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Representa un grupo de secuencias[`Revision`](../revision/) objetos.

Para obtener más información, visite el[Seguimiento de cambios en un documento](https://docs.aspose.com/words/net/track-changes-in-a-document/) Artículo de documentación.

```csharp
public class RevisionGroup
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Obtiene el autor de este grupo de revisión. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Obtiene el tipo de revisiones incluidas en este grupo. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Devuelve el texto insertado/eliminado/movido o la descripción del cambio de formato. |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
