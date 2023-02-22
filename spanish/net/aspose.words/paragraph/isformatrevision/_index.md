---
title: Paragraph.IsFormatRevision
second_title: Referencia de API de Aspose.Words para .NET
description: Paragraph propiedad. Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios.
type: docs
weight: 90
url: /es/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios.

```csharp
public bool IsFormatRevision { get; }
```

### Ejemplos

Muestra cómo verificar si un párrafo es una revisión de formato.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Este párrafo es una revisión de "Formato", que ocurre cuando cambiamos el formato del texto existente
// mientras realiza un seguimiento de las revisiones en Microsoft Word a través de "Revisar" -> "Cambio de camino".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../paragraph/)
* asamblea [Aspose.Words](../../../)


