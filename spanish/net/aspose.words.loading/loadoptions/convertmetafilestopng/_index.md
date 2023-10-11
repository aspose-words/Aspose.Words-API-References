---
title: LoadOptions.ConvertMetafilesToPng
second_title: Referencia de API de Aspose.Words para .NET
description: LoadOptions propiedad. Obtiene o establece si se debe convertir el metarchivo Wmf oEmf  imágenes aPng formato de imagen.
type: docs
weight: 30
url: /es/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Obtiene o establece si se debe convertir el metarchivo (Wmf oEmf ) imágenes aPng formato de imagen.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

### Observaciones

Metarchivos (Wmf oEmf ) es un formato de imagen sin comprimir y a veces requiere demasiada RAM para almacenar y procesar el documento. Esta opción permite convertir todas las imágenes de metarchivo aPng al cargar el documento. Tenga en cuenta que la conversión de gráficos vectoriales a rasterizados disminuye la calidad de las imágenes.

### Ejemplos

Muestra cómo convertir WMF/EMF a PNG durante la carga del documento.

```csharp
Document doc = new Document();

            Shape shape = new Shape(doc, ShapeType.Image);
            shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
            shape.Width = 100;
            shape.Height = 100;

            doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

            doc.Save(ArtifactsDir + "Image.CreateImageDirectly.docx");

            shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

            TestUtil.VerifyImageInShape(1600, 1600, ImageType.Wmf, shape);

            LoadOptions loadOptions = new LoadOptions();
            loadOptions.ConvertMetafilesToPng = true;

            doc = new Document(ArtifactsDir + "Image.CreateImageDirectly.docx", loadOptions);
            shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

#if NET48
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#elif NET5_0_OR_GREATER
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#endif
```

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../loadoptions/)
* asamblea [Aspose.Words](../../../)


