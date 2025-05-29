---
title: DocSaveOptions.SavePictureBullet
linktitle: SavePictureBullet
articleTitle: SavePictureBullet
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad DocSaveOptions SavePictureBullet mejora la salida de sus documentos. Controle fácilmente el guardado de datos de PictureBullet para obtener resultados óptimos.
type: docs
weight: 60
url: /es/net/aspose.words.saving/docsaveoptions/savepicturebullet/
---
## DocSaveOptions.SavePictureBullet property

Cuando`FALSO` , Los datos de PictureBullet no se guardan en el documento de salida. El valor predeterminado es`verdadero` .

```csharp
public bool SavePictureBullet { get; set; }
```

## Observaciones

Esta opción se proporciona para Word 97, que no puede funcionar correctamente con datos de PictureBullet. Para eliminar los datos de PictureBullet, configure la opción en "falso".

## Ejemplos

Muestra cómo omitir los datos de PictureBullet del documento al guardarlo.

```csharp
Document doc = new Document(MyDir + "Image bullet points.docx");
//Algunos procesadores de texto, como Microsoft Word 97, son incompatibles con los datos de PictureBullet.
// Al establecer una bandera en el objeto SaveOptions,
//podemos convertir todas las viñetas de imágenes en viñetas normales al guardarlas.
DocSaveOptions saveOptions = new DocSaveOptions(SaveFormat.Doc);
saveOptions.SavePictureBullet = false;

doc.Save(ArtifactsDir + "DocSaveOptions.PictureBullets.doc", saveOptions);
```

### Ver también

* class [DocSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
