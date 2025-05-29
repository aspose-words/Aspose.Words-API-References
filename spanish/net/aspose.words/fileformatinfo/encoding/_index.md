---
title: FileFormatInfo.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words para .NET
description: Descubra la propiedad de codificación FileFormatInfo para identificar fácilmente la codificación de documentos. Actualmente admite formatos HTML para obtener resultados precisos.
type: docs
weight: 10
url: /es/net/aspose.words/fileformatinfo/encoding/
---
## FileFormatInfo.Encoding property

Obtiene la codificación detectada si es aplicable al formato del documento actual. Por el momento, solo detecta codificación para documentos HTML.

```csharp
public Encoding Encoding { get; }
```

## Ejemplos

Muestra cómo detectar la codificación en un archivo html.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// La propiedad Encoding se utiliza solo cuando creamos un objeto FileFormatInfo para un documento html.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Ver también

* class [FileFormatInfo](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
