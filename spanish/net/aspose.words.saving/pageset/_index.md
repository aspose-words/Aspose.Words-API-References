---
title: PageSet Class
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.PageSet para una gestión eficiente de documentos. ¡Defina fácilmente conjuntos de páginas aleatorios y mejore su flujo de trabajo hoy mismo!
type: docs
weight: 6170
url: /es/net/aspose.words.saving/pageset/
---
## PageSet class

Describe un conjunto aleatorio de páginas.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) Artículo de documentación.

```csharp
public sealed class PageSet : IEnumerable<int>
```

## Constructores

| Nombre | Descripción |
| --- | --- |
| [PageSet](pageset/#constructor_1)(*int*) | Crea un conjunto de una página basado en el índice de página exacto. |
| [PageSet](pageset/#constructor_2)(*params int[]*) | Crea un conjunto de páginas basado en índices de página exactos. |
| [PageSet](pageset/#constructor)(*params PageRange[]*) | Crea un conjunto de páginas basado en rangos. |

## Propiedades

| Nombre | Descripción |
| --- | --- |
| static [All](../../aspose.words.saving/pageset/all/) { get; } | Obtiene un conjunto con todas las páginas del documento en su orden original. |
| static [Even](../../aspose.words.saving/pageset/even/) { get; } | Obtiene un conjunto con todas las páginas pares del documento en su orden original. |
| static [Odd](../../aspose.words.saving/pageset/odd/) { get; } | Obtiene un conjunto con todas las páginas impares del documento en su orden original. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [GetEnumerator](../../aspose.words.saving/pageset/getenumerator/)() |  |

## Ejemplos

Muestra cómo convertir una página de un documento en una imagen JPEG.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1.");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2.");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3.");

// Crea un objeto "ImageSaveOptions" que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento en una imagen.
ImageSaveOptions options = new ImageSaveOptions(SaveFormat.Jpeg);
// Establezca "PageSet" en "1" para seleccionar la segunda página mediante
// el índice basado en cero desde el cual comenzar a renderizar el documento.
options.PageSet = new PageSet(1);

// Cuando guardamos el documento en formato JPEG, Aspose.Words solo renderiza una página.
//Esta imagen contendrá una página a partir de la página dos,
// que será sólo la segunda página del documento original.
doc.Save(ArtifactsDir + "ImageSaveOptions.OnePage.jpg", options);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
