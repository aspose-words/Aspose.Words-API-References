---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words para .NET
description: Cree un conjunto de páginas personalizado sin esfuerzo con el constructor PageSet, diseñado para una indexación de páginas precisa y una experiencia de usuario perfecta.
type: docs
weight: 10
url: /es/net/aspose.words.saving/pageset/pageset/
---
## PageSet(*int*) {#constructor_1}

Crea un conjunto de una página basado en el índice de página exacto.

```csharp
public PageSet(int page)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| page | Int32 | Índice basado en cero de la página. |

## Observaciones

Si se encuentra una página que no está en el documento, se lanzará una excepción durante la representación. MaxValue significa la última página del documento.

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

* class [PageSet](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)

---

## PageSet(*params int[]*) {#constructor_2}

Crea un conjunto de páginas basado en índices de página exactos.

```csharp
public PageSet(params int[] pages)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| pages | Int32[] | Índices de páginas basados en cero. |

## Observaciones

Si se encuentra una página que no está en el documento, se lanzará una excepción durante la representación. MaxValue significa la última página del documento.

## Ejemplos

Muestra cómo extraer páginas basándose en índices de página exactos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//Añadir cinco páginas al documento.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Crea un objeto "XpsSaveOptions", que podemos pasar al método "Guardar" del documento
// para modificar la forma en que ese método convierte el documento a .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Utilice la propiedad "PageSet" para seleccionar un conjunto de páginas del documento para guardar en la salida XPS.
// En este caso, elegiremos, mediante un índice basado en cero, solo tres páginas: página 1, página 2 y página 4.
xpsOptions.PageSet = new PageSet(0, 1, 3);

doc.Save(ArtifactsDir + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

### Ver también

* class [PageSet](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)

---

## PageSet(*params PageRange[]*) {#constructor}

Crea un conjunto de páginas basado en rangos.

```csharp
public PageSet(params PageRange[] ranges)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| ranges | PageRange[] | Matriz de rangos de páginas. |

## Observaciones

Si se encuentra un rango que comienza después de la última página del documento, se lanzará una excepción durante la representación. Todos los rangos que terminan después de la última página se truncan para que quepan en el documento.

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

* class [PageRange](../../pagerange/)
* class [PageSet](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
