---
title: Document.OriginalLoadFormat
linktitle: OriginalLoadFormat
articleTitle: OriginalLoadFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad OriginalLoadFormat para acceder fácilmente al formato del documento original cargado en su objeto, mejorando la gestión de documentos.
type: docs
weight: 310
url: /es/net/aspose.words/document/originalloadformat/
---
## Document.OriginalLoadFormat property

Obtiene el formato del documento original que se cargó en este objeto.

```csharp
public LoadFormat OriginalLoadFormat { get; }
```

## Observaciones

Si ha creado un nuevo documento en blanco, devuelve elDoc valor.

## Ejemplos

Muestra cómo recuperar detalles de la operación de carga de un documento.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(MyDir + "Document.docx", doc.OriginalFileName);
Assert.AreEqual(LoadFormat.Docx, doc.OriginalLoadFormat);
```

### Ver también

* enum [LoadFormat](../../loadformat/)
* class [Document](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
