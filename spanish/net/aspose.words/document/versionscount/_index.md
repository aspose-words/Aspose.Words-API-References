---
title: Document.VersionsCount
linktitle: VersionsCount
articleTitle: VersionsCount
second_title: Aspose.Words para .NET
description: Descubra la propiedad Document VersionsCount para rastrear fácilmente la cantidad de versiones de documentos almacenadas en sus archivos DOC para una mejor administración y organización.
type: docs
weight: 480
url: /es/net/aspose.words/document/versionscount/
---
## Document.VersionsCount property

Obtiene el número de versiones del documento que se almacenaron en el documento DOC.

```csharp
public int VersionsCount { get; }
```

## Observaciones

Se accede a las versiones en Microsoft Word mediante el menú Archivo/Versiones. Microsoft Word solo admite versiones para archivos DOC.

Esta propiedad permite detectar si existían versiones del documento almacenadas en este documento antes de abrirlo en Aspose.Words. Aspose.Words no ofrece ninguna otra compatibilidad con versiones de documentos. Si guarda este documento con Aspose.Words, se guardará sin versiones.

## Ejemplos

Muestra cómo trabajar con la función de conteo de versiones de documentos antiguos de Microsoft Word.

```csharp
Document doc = new Document(MyDir + "Versions.doc");

//Podemos leer esta propiedad de un documento, pero no podemos conservarla al guardarla.
Assert.AreEqual(4, doc.VersionsCount);

doc.Save(ArtifactsDir + "Document.VersionsCount.doc");
doc = new Document(ArtifactsDir + "Document.VersionsCount.doc");

Assert.AreEqual(0, doc.VersionsCount);
```

### Ver también

* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
