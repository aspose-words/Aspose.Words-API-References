---
title: Paragraph.IsFormatRevision
linktitle: IsFormatRevision
articleTitle: IsFormatRevision
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad IsFormatRevision en Microsoft Word rastrea los cambios de formato, lo que garantiza ediciones precisas del documento y una colaboración mejorada.
type: docs
weight: 90
url: /es/net/aspose.words/paragraph/isformatrevision/
---
## Paragraph.IsFormatRevision property

Devuelve verdadero si se cambió el formato del objeto en Microsoft Word mientras estaba habilitado el seguimiento de cambios.

```csharp
public bool IsFormatRevision { get; }
```

## Ejemplos

Muestra cómo comprobar si un párrafo es una revisión de formato.

```csharp
Document doc = new Document(MyDir + "Format revision.docx");

// Este párrafo es una revisión de "Formato", que ocurre cuando cambiamos el formato del texto existente.
// mientras se realiza el seguimiento de revisiones en Microsoft Word a través de "Revisar" -> "Seguimiento de cambios".
Assert.True(doc.FirstSection.Body.FirstParagraph.IsFormatRevision);
```

### Ver también

* class [Paragraph](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
