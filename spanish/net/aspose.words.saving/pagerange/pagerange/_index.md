---
title: PageRange.PageRange
second_title: Referencia de API de Aspose.Words para .NET
description: PageRange constructor. Crea un nuevo objeto de rango de páginas.
type: docs
weight: 10
url: /es/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

Crea un nuevo objeto de rango de páginas.

```csharp
public PageRange(int from, int to)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| from | Int32 | La página de inicio índice de base cero. |
| to | Int32 | El índice de base cero de la página final. Si supera el índice de la última página del documento, se trunca para que quepa en el documento al renderizar. |

### Observaciones

MaxValue significa la última página del documento.

### Ejemplos

Muestra cómo extraer páginas en función de intervalos de páginas exactos.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Ver también

* class [PageRange](../)
* espacio de nombres [Aspose.Words.Saving](../../pagerange/)
* asamblea [Aspose.Words](../../../)


