---
title: RevisionCollection.AcceptAll
linktitle: AcceptAll
articleTitle: AcceptAll
second_title: Aspose.Words para .NET
description: Descubra el método AcceptAll de RevisionCollection para integrar sin problemas todas las revisiones, mejorando la eficiencia de su flujo de trabajo y la colaboración.
type: docs
weight: 50
url: /es/net/aspose.words/revisioncollection/acceptall/
---
## RevisionCollection.AcceptAll method

Acepta todas las revisiones de esta colección.

```csharp
public void AcceptAll()
```

## Ejemplos

Muestra cómo comparar documentos.

```csharp
Document docOriginal = new Document();
DocumentBuilder builder = new DocumentBuilder(docOriginal);
builder.Writeln("This is the original document.");

Document docEdited = new Document();
builder = new DocumentBuilder(docEdited);
builder.Writeln("This is the edited document.");

// Comparar documentos con revisiones generará una excepción.
if (docOriginal.Revisions.Count == 0 && docEdited.Revisions.Count == 0)
    docOriginal.Compare(docEdited, "authorName", DateTime.Now);

//Después de la comparación, el documento original obtendrá una nueva revisión
// para cada elemento que sea diferente en el documento editado.
foreach (Revision r in docOriginal.Revisions)
{
    Console.WriteLine($"Revision type: {r.RevisionType}, on a node of type \"{r.ParentNode.NodeType}\"");
    Console.WriteLine($"\tChanged text: \"{r.ParentNode.GetText()}\"");
}

//Aceptar estas revisiones transformará el documento original en el documento editado.
docOriginal.Revisions.AcceptAll();

Assert.AreEqual(docOriginal.GetText(), docEdited.GetText());
```

### Ver también

* class [RevisionCollection](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
