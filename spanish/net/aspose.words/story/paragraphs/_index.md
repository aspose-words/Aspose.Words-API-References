---
title: Story.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words para .NET
description: Descubre los párrafos de tu historia. Accede a una colección de párrafos seleccionados directamente desde tu historia y enriquece tu narrativa con contenido rico y atractivo.
type: docs
weight: 30
url: /es/net/aspose.words/story/paragraphs/
---
## Story.Paragraphs property

Obtiene una colección de párrafos que son hijos inmediatos de la historia.

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../paragraphcollection/)
* class [Story](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
