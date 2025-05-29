---
title: Paragraph.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words para .NET
description: ¡Descubre la propiedad IsMoveToRevision en Microsoft Word! Aprende cómo controla los cambios y mejora tu experiencia de edición de documentos.
type: docs
weight: 140
url: /es/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

Devuelve`verdadero` Si este objeto se movió (insertó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```csharp
public bool IsMoveToRevision { get; }
```

## Ejemplos

Muestra cómo comprobar si un párrafo es una revisión de movimiento.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Este documento contiene revisiones "Mover", que aparecen cuando resaltamos texto con el cursor,
// y luego arrástrelo para moverlo a otra ubicación
// mientras se realiza el seguimiento de revisiones en Microsoft Word a través de "Revisar" -> "Seguimiento de cambios".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Las revisiones de movimiento constan de pares de revisiones "Mover desde" y "Mover a".
//Estas revisiones son cambios potenciales al documento que podemos aceptar o rechazar.
// Antes de aceptar o rechazar una revisión de movimiento, el documento
// debe realizar un seguimiento de los destinos de salida y llegada del texto.
// El segundo y el cuarto párrafo definen una de esas revisiones y, por lo tanto, ambos tienen el mismo contenido.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// La revisión "Mover desde" es el párrafo desde donde arrastramos el texto.
// Si aceptamos la revisión, este párrafo desaparecerá,
// y el otro permanecerá y ya no será una revisión.
Assert.True(paragraphs[1].IsMoveFromRevision);

//La revisión "Mover a" es el párrafo donde arrastramos el texto.
// Si rechazamos la revisión, este párrafo desaparecerá y el otro permanecerá.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
