---
title: Class RevisionGroup
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.RevisionGroup clase. Representa un grupo de secuencialesRevision objetos.
type: docs
weight: 4520
url: /es/net/aspose.words/revisiongroup/
---
## RevisionGroup class

Representa un grupo de secuenciales[`Revision`](../revision/) objetos.

```csharp
public class RevisionGroup
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Author](../../aspose.words/revisiongroup/author/) { get; } | Obtiene el autor de este grupo de revisión. |
| [RevisionType](../../aspose.words/revisiongroup/revisiontype/) { get; } | Obtiene el tipo de revisiones incluidas en este grupo. |
| [Text](../../aspose.words/revisiongroup/text/) { get; } | Devuelve texto insertado/eliminado/movido o descripción del cambio de formato. |

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)


