---
title: Document.VersionsCount
second_title: Referencia de API de Aspose.Words para .NET
description: Document propiedad. Obtiene el número de versiones del documento que se almacenó en el documento DOC.
type: docs
weight: 440
url: /es/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Obtiene el número de versiones del documento que se almacenó en el documento DOC.

```csharp
public int VersionsCount { get; }
```

### Observaciones

Se accede a las versiones en Microsoft Word a través del menú Archivo/Versiones. Microsoft Word admite versiones solo para archivos DOC.

Esta propiedad permite detectar si había versiones de documentos almacenadas en este documento antes de que se abriera en Aspose.Words. Aspose.Words no proporciona ningún otro soporte para versiones de documentos. Si guarda este documento usando Aspose.Words, el documento se guardará sin versiones.

### Ejemplos

Muestra cómo trabajar con la función de conteo de versiones de documentos antiguos de Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

// Podemos leer esta propiedad de un documento, pero no podemos conservarla mientras se guarda.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");      
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../document/)
* asamblea [Aspose.Words](../../../)


