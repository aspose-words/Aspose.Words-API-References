---
title: Range.Revisions
linktitle: Revisions
articleTitle: Revisions
second_title: Aspose.Words para .NET
description: Descubra las Revisiones de Gama. Realice un seguimiento y gestione fácilmente los cambios en la propiedad con nuestra completa colección de revisiones para una mayor claridad en el proyecto.
type: docs
weight: 40
url: /es/net/aspose.words/range/revisions/
---
## Range.Revisions property

Obtiene una colección de revisiones (cambios rastreados) que existen en este rango.

```csharp
public RevisionCollection Revisions { get; }
```

## Observaciones

La colección devuelta es una colección "viva", lo que significa que si elimina partes de un documento que contienen revisiones, las revisiones eliminadas desaparecerán automáticamente de esta colección.

## Ejemplos

Muestra cómo trabajar con revisiones dentro del rango.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
foreach (Revision revision in paragraph.Range.Revisions)
{
    if (revision.RevisionType == RevisionType.Deletion)
        revision.Accept();
}

// Rechazar las revisiones de la primera sección.
doc.FirstSection.Range.Revisions.RejectAll();
```

### Ver también

* class [RevisionCollection](../../revisioncollection/)
* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
