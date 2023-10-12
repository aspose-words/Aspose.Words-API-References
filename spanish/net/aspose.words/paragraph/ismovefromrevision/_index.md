---
title: Paragraph.IsMoveFromRevision
second_title: Referencia de API de Aspose.Words para .NET
description: Paragraph propiedad. Devolucionesverdadero si este objeto se movió eliminó en Microsoft Word mientras el seguimiento de cambios estaba habilitado.
type: docs
weight: 130
url: /es/net/aspose.words/paragraph/ismovefromrevision/
---
## Paragraph.IsMoveFromRevision property

Devoluciones`verdadero` si este objeto se movió (eliminó) en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```csharp
public bool IsMoveFromRevision { get; }
```

### Ejemplos

Muestra cómo comprobar si un párrafo es una revisión movida.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Este documento contiene revisiones "Mover", que aparecen cuando resaltamos texto con el cursor,
// y luego arrástrelo para moverlo a otra ubicación
// mientras realizamos el seguimiento de las revisiones en Microsoft Word mediante "Revisar" -> "Cambio de camino".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Las revisiones de movimiento constan de pares de revisiones "Mover desde" y "Mover a".
// Estas revisiones son cambios potenciales al documento que podemos aceptar o rechazar.
// Antes de aceptar/rechazar una revisión de movimiento, el documento
// debe realizar un seguimiento de los destinos de salida y llegada del texto.
// El segundo y cuarto párrafo definen una de esas revisiones y, por lo tanto, ambos tienen el mismo contenido.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// La revisión "Mover desde" es el párrafo desde donde arrastramos el texto.
// Si aceptamos la revisión, este párrafo desaparecerá,
// y el otro permanecerá y ya no será una revisión.
Assert.True(paragraphs[1].IsMoveFromRevision);

// La revisión "Mover a" es el párrafo donde arrastramos el texto.
// Si rechazamos la revisión, este párrafo desaparecerá y el otro permanecerá.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../paragraph/)
* asamblea [Aspose.Words](../../../)


