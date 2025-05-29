---
title: BuiltInDocumentProperties.HyperlinksChanged
linktitle: HyperlinksChanged
articleTitle: HyperlinksChanged
second_title: Aspose.Words para .NET
description: Descubra la propiedad BuiltInDocumentProperties HyperlinksChanged, que rastrea los cambios en los hipervínculos en sus documentos para un mejor control de edición.
type: docs
weight: 130
url: /es/net/aspose.words.properties/builtindocumentproperties/hyperlinkschanged/
---
## BuiltInDocumentProperties.HyperlinksChanged property

Indica si se cambiaron los hipervínculos en un documento.

```csharp
public bool HyperlinksChanged { get; }
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
