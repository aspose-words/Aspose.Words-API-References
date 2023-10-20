---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words para .NET
description: LoadOptions BaseUri propiedad. Obtiene o establece la cadena que se utilizará para resolver los URI relativos que se encuentran en el documento en URI absolutos cuando sea necesario. Puede sernulo o cadena vacía. El valor predeterminado esnulo  en C#.
type: docs
weight: 20
url: /es/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Obtiene o establece la cadena que se utilizará para resolver los URI relativos que se encuentran en el documento en URI absolutos cuando sea necesario. Puede ser`nulo` o cadena vacía. El valor predeterminado es`nulo` .

```csharp
public string BaseUri { get; set; }
```

## Observaciones

Esta propiedad se utiliza para convertir URI relativos en absolutos en los siguientes casos:

1. Cuando se carga un documento HTML desde una secuencia y el documento contiene imágenes con URI relativos y no tiene un URI base especificado en el elemento HTML BASE.
2. Al guardar un documento en PDF y otros formatos, para recuperar imágenes vinculadas mediante URI relativos para que las imágenes se puedan guardar en el documento de salida.

## Ejemplos

Muestra cómo abrir un documento HTML con imágenes de una secuencia utilizando un URI base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Pasa el URI de la carpeta base mientras la cargas
    // para que se puedan encontrar todas las imágenes con URI relativos en el documento HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifica que la primera forma del documento contenga una imagen válida.
    Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

    Assert.IsTrue(shape.IsImage);
    Assert.IsNotNull(shape.ImageData.ImageBytes);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Width), 0.01);
    Assert.AreEqual(32.0, ConvertUtil.PointToPixel(shape.Height), 0.01);
}
```

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
