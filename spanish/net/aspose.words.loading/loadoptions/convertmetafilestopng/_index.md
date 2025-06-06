---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: Aspose.Words para .NET
description: Convierta fácilmente metarchivos WMF y EMF a formato PNG con LoadOptions. ¡Simplifique la gestión de imágenes y mejore la compatibilidad hoy mismo!
type: docs
weight: 30
url: /es/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Obtiene o establece si se debe convertir el metarchivo(Wmf oEmf ) imágenes aPngformato de imagen.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## Observaciones

Metarchivos (Wmf oEmf ) es un formato de imagen sin comprimir y a veces requiere mucha RAM para almacenar y procesar el documento. Esta opción permite convertir todas las imágenes de metarchivo aPng al cargar el documento. Tenga en cuenta que la conversión de gráficos vectoriales a raster disminuye la calidad de las imágenes.

## Ejemplos

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

TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
```

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
