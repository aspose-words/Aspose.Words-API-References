---
title: RevisionGroup.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words para .NET
description: RevisionGroup Text propiedad. Devuelve texto insertado/eliminado/movido o descripción del cambio de formato en C#.
type: docs
weight: 30
url: /es/net/aspose.words/revisiongroup/text/
---
## RevisionGroup.Text property

Devuelve texto insertado/eliminado/movido o descripción del cambio de formato.

```csharp
public string Text { get; }
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

* class [RevisionGroup](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
