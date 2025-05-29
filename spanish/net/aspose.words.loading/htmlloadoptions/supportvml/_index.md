---
title: HtmlLoadOptions.SupportVml
linktitle: SupportVml
articleTitle: SupportVml
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlLoadOptions SupportVml mejora su experiencia web al habilitar la compatibilidad con imágenes VML para una mejor calidad de gráficos.
type: docs
weight: 70
url: /es/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

Obtiene o establece un valor que indica si se deben admitir imágenes VML.

```csharp
public bool SupportVml { get; set; }
```

## Ejemplos

Muestra cómo admitir comentarios condicionales al cargar un documento HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Si el valor es verdadero, tomamos en cuenta el código VML al analizar el documento cargado.
loadOptions.SupportVml = supportVml;

// Este documento contiene una imagen JPEG dentro de las etiquetas "<!--[if gte vml 1]>",
// y una imagen PNG diferente dentro de las etiquetas "<![if !vml]>".
// Si establecemos el indicador "SupportVml" en "verdadero", entonces Aspose.Words cargará el JPEG.
// Si establecemos esta bandera como "falso", entonces Aspose.Words solo cargará el PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Ver también

* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
