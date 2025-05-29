---
title: Comparer.CompareToImages
linktitle: CompareToImages
articleTitle: CompareToImages
second_title: Aspose.Words para .NET
description: Compare documentos sin esfuerzo con CompareToImages, guardando las diferencias como imágenes para cada página, mejorando la claridad y el análisis visual.
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/comparer/comparetoimages/
---
## CompareToImages(*string, string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages_1}

Compara dos documentos y guarda las diferencias como imágenes. Cada elemento de la matriz devuelta representa una sola página de la salida representada como una imagen.

```csharp
public static Stream[] CompareToImages(string v1, string v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| v1 | String | El documento original. |
| v2 | String | El documento modificado. |
| imageSaveOptions | ImageSaveOptions | Opciones para guardar la imagen de salida. |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y hora que se utilizarán para las revisiones. |
| compareOptions | CompareOptions | Opciones de comparación de documentos. |

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## CompareToImages(*Stream, Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#comparetoimages}

Compara dos documentos y guarda las diferencias como imágenes. Cada elemento de la matriz devuelta representa una sola página de la salida representada como una imagen.

```csharp
public static Stream[] CompareToImages(Stream v1, Stream v2, ImageSaveOptions imageSaveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| v1 | Stream | El documento original. |
| v2 | Stream | El documento modificado. |
| imageSaveOptions | ImageSaveOptions | Opciones para guardar la imagen de salida. |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y hora que se utilizarán para las revisiones. |
| compareOptions | CompareOptions | Opciones de comparación de documentos. |

## Ejemplos

Muestra cómo comparar documentos y guardar resultados como imágenes.

```csharp
//Hay varias formas de comparar documentos:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Stream[] pages = Comparer.CompareToImages(firstDoc, secondDoc, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime());

using (FileStream firstStreamIn = new FileStream(firstDoc, FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(secondDoc, FileMode.Open, FileAccess.Read))
    {
        CompareOptions compareOptions = new CompareOptions();
        compareOptions.IgnoreCaseChanges = true;
        pages = Comparer.CompareToImages(firstStreamIn, secondStreamIn, new ImageSaveOptions(SaveFormat.Png), "Author", new DateTime(), compareOptions);
    }
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
