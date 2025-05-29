---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.PageRange para definir fácilmente rangos de páginas continuos. Mejore el procesamiento de sus documentos con precisión y eficiencia.
type: docs
weight: 6150
url: /es/net/aspose.words.saving/pagerange/
---
## PageRange class

Representa un rango continuo de páginas.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) Artículo de documentación.

```csharp
public sealed class PageRange
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | Crea un nuevo objeto de rango de páginas. |

## Ejemplos

Muestra cómo extraer páginas según rangos de páginas exactos.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
