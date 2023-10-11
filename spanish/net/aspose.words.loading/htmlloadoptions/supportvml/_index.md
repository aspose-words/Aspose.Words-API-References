---
title: HtmlLoadOptions.SupportVml
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlLoadOptions propiedad. Obtiene o establece un valor que indica si se admiten imágenes VML.
type: docs
weight: 60
url: /es/net/aspose.words.loading/htmlloadoptions/supportvml/
---
## HtmlLoadOptions.SupportVml property

Obtiene o establece un valor que indica si se admiten imágenes VML.

```csharp
public bool SupportVml { get; set; }
```

### Ejemplos

Muestra cómo admitir comentarios condicionales al cargar un documento HTML.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Si el valor es verdadero, tomamos en cuenta el código VML al analizar el documento cargado.
loadOptions.SupportVml = supportVml;

// Este documento contiene una imagen JPEG dentro de "<!--[if gte vml 1]>" etiquetas,
// y una imagen PNG diferente dentro de "<![if !vml]>" etiquetas.
// Si configuramos el indicador "SupportVml" en "true", Aspose.Words cargará el JPEG.
// Si configuramos este indicador en "falso", entonces Aspose.Words solo cargará el PNG.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Ver también

* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../htmlloadoptions/)
* asamblea [Aspose.Words](../../../)


