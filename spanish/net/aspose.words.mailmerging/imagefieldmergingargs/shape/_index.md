---
title: ImageFieldMergingArgs.Shape
second_title: Referencia de API de Aspose.Words para .NET
description: ImageFieldMergingArgs propiedad. Especifica la forma que el motor de combinación de correspondencia debe insertar en el documento.
type: docs
weight: 60
url: /es/net/aspose.words.mailmerging/imagefieldmergingargs/shape/
---
## ImageFieldMergingArgs.Shape property

Especifica la forma que el motor de combinación de correspondencia debe insertar en el documento.

```csharp
public Shape Shape { get; set; }
```

### Observaciones

Cuando se especifica esta propiedad, el motor de combinación de correspondencia ignora todas las demás propiedades como[`ImageFileName`](../imagefilename/) o[`ImageStream`](../imagestream/) y simplemente inserta la forma en el documento.

Utilice esta propiedad para controlar completamente el proceso de combinación de un campo de combinación de imágenes. Por ejemplo, puede especificar[`WrapType`](../../../aspose.words.drawing/shapebase/wraptype/) o cualquier otra propiedad de forma para ajustar el nodo resultante. Sin embargo, tenga en cuenta que usted es responsable de proporcionar el contenido de la forma.

### Ver también

* class [Shape](../../../aspose.words.drawing/shape/)
* class [ImageFieldMergingArgs](../)
* espacio de nombres [Aspose.Words.MailMerging](../../imagefieldmergingargs/)
* asamblea [Aspose.Words](../../../)


