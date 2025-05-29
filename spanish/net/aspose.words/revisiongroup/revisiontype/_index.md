---
title: RevisionGroup.RevisionType
linktitle: RevisionType
articleTitle: RevisionType
second_title: Aspose.Words para .NET
description: Descubra la propiedad RevisionType de RevisionGroup para identificar y gestionar fácilmente los tipos de revisiones en su proyecto. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words/revisiongroup/revisiontype/
---
## RevisionGroup.RevisionType property

Obtiene el tipo de revisiones incluidas en este grupo.

```csharp
public RevisionType RevisionType { get; }
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

* enum [RevisionType](../../revisiontype/)
* class [RevisionGroup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
