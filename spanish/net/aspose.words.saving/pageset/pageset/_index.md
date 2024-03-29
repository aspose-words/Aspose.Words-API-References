---
title: PageSet
linktitle: PageSet
articleTitle: PageSet
second_title: Aspose.Words para .NET
description: PageSet constructor. Crea un conjunto de una página basado en el índice de página exacto en C#.
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
| page | Int32 | Índice de base cero de la página. |

## Observaciones

Si se encuentra una página que no está en el documento, se generará una excepción durante la representación. MaxValue significa la última página del documento.

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
| pages | Int32[] | Índices de páginas de base cero. |

## Observaciones

Si se encuentra una página que no está en el documento, se generará una excepción durante la representación. MaxValue significa la última página del documento.

## Ejemplos

Muestra cómo extraer páginas basándose en índices de páginas exactos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agrega cinco páginas al documento.
for (int i = 1; i < 6; i++)
{
    builder.Write("Page " + i);
    builder.InsertBreak(BreakType.PageBreak);
}

// Crea un objeto "XpsSaveOptions", que podemos pasar al método "Guardar" del documento.
// para modificar cómo ese método convierte el documento a .XPS.
XpsSaveOptions xpsOptions = new XpsSaveOptions();

// Utilice la propiedad "PageSet" para seleccionar un conjunto de páginas del documento para guardar en XPS de salida.
// En este caso, elegiremos, mediante un índice de base cero, solo tres páginas: página 1, página 2 y página 4.
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

Si se encuentra un rango que comienza después de la última página del documento, se generará una excepción durante la representación. Todos los rangos que terminan después de la última página se truncan para caber en el documento.

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
