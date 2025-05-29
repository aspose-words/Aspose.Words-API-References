---
title: BuiltInDocumentProperties.ScaleCrop
linktitle: ScaleCrop
articleTitle: ScaleCrop
second_title: Aspose.Words para .NET
description: Descubra la propiedad ScaleCrop en BuiltInDocumentProperties, que controla la visualización de miniaturas, lo que garantiza una visualización óptima con imágenes recortadas o escaladas.
type: docs
weight: 260
url: /es/net/aspose.words.properties/builtindocumentproperties/scalecrop/
---
## BuiltInDocumentProperties.ScaleCrop property

Indica si la miniatura del documento está recortada o escalada para ajustarse a la pantalla.

```csharp
public bool ScaleCrop { get; }
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
