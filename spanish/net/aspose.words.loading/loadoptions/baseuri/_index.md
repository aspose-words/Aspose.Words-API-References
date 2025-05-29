---
title: LoadOptions.BaseUri
linktitle: BaseUri
articleTitle: BaseUri
second_title: Aspose.Words para .NET
description: Descubra la propiedad LoadOptions BaseUri para convertir fácilmente URIs relativas a absolutas en sus documentos. ¡Mejore su gestión de URIs hoy mismo!
type: docs
weight: 20
url: /es/net/aspose.words.loading/loadoptions/baseuri/
---
## LoadOptions.BaseUri property

Obtiene o establece la cadena que se utilizará para resolver los URI relativos encontrados en el documento en URI absolutos cuando sea necesario. Puede ser`nulo` o cadena vacía. El valor predeterminado es`nulo` .

```csharp
public string BaseUri { get; set; }
```

## Observaciones

Esta propiedad se utiliza para resolver URI relativos en absolutos en los siguientes casos:

1. Al cargar un documento HTML desde una secuencia y el documento contiene imágenes con URI relativas y no tiene una URI base especificada en el elemento HTML BASE.
2. Al guardar un documento en PDF y otros formatos, para recuperar imágenes vinculadas mediante URI relativas para que las imágenes se puedan guardar en el documento de salida.

## Ejemplos

Muestra cómo abrir un documento HTML con imágenes desde una transmisión usando una URI base.

```csharp
using (Stream stream = File.OpenRead(MyDir + "Document.html"))
{
    // Pasar la URI de la carpeta base mientras se carga
    // para que se puedan encontrar todas las imágenes con URI relativas en el documento HTML.
    LoadOptions loadOptions = new LoadOptions();
    loadOptions.BaseUri = ImageDir;

    Document doc = new Document(stream, loadOptions);

    // Verifique que la primera forma del documento contenga una imagen válida.
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
