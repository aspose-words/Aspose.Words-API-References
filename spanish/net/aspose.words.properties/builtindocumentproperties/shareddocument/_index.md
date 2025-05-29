---
title: BuiltInDocumentProperties.SharedDocument
linktitle: SharedDocument
articleTitle: SharedDocument
second_title: Aspose.Words para .NET
description: Descubra la función BuiltInDocumentProperties SharedDocument que revela si su documento está compartido, lo que mejora la colaboración y la accesibilidad.
type: docs
weight: 280
url: /es/net/aspose.words.properties/builtindocumentproperties/shareddocument/
---
## BuiltInDocumentProperties.SharedDocument property

Indica si el documento es un documento compartido.

```csharp
public bool SharedDocument { get; }
```

## Observaciones

Aspose.Words no actualiza esta propiedad.

## Ejemplos

Muestra cómo obtener propiedades ampliadas.

```csharp
Document doc = new Document(MyDir + "Extended properties.docx");
Assert.IsTrue(doc.BuiltInDocumentProperties.ScaleCrop);
Assert.IsTrue(doc.BuiltInDocumentProperties.SharedDocument);
Assert.IsTrue(doc.BuiltInDocumentProperties.HyperlinksChanged);
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
