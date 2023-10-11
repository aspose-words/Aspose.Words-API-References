---
title: Range.Revisions
second_title: Referencia de API de Aspose.Words para .NET
description: Range propiedad. Obtiene una colección de revisiones cambios rastreados que existen en este rango.
type: docs
weight: 40
url: /es/net/aspose.words/range/revisions/
---
## Range.Revisions property

Obtiene una colección de revisiones (cambios rastreados) que existen en este rango.

```csharp
public RevisionCollection Revisions { get; }
```

### Observaciones

La colección devuelta es una colección "activa", lo que significa que si elimina partes de un documento que contiene revisiones, las revisiones eliminadas desaparecerán automáticamente de esta colección.

### Ejemplos

Muestra cómo trabajar con revisiones dentro del rango.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// Rechaza las revisiones de la primera sección.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Ver también

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* espacio de nombres [Aspose.Words](../../range/)
* asamblea [Aspose.Words](../../../)


