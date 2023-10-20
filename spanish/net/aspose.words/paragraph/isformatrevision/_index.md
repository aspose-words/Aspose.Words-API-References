---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words para .NET
description: Paragraph IsFormatRevision propiedad. Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras el seguimiento de cambios estaba habilitado en C#.
type: docs
weight: 90
url: /es/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras el seguimiento de cambios estaba habilitado.

```csharp
public bool IsFormatRevision { get; }
```

## Ejemplos

Muestra cómo comprobar si un párrafo es una revisión de formato.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Este párrafo es una revisión de "Formato", que ocurre cuando cambiamos el formato del texto existente
// mientras realizamos el seguimiento de las revisiones en Microsoft Word mediante "Revisar" -> "Cambio de camino".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
