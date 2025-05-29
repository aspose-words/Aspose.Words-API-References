---
title: Comparer.Compare
linktitle: Compare
articleTitle: Compare
second_title: Aspose.Words para .NET
description: Compare fácilmente dos documentos con nuestro método Comparar. Guarde las diferencias y registre las ediciones y revisiones de formato en un solo archivo de salida.
type: docs
weight: 20
url: /es/net/aspose.words.lowcode/comparer/compare/
---
## Compare(*string, string, string, string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_4}

Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado, produciendo cambios como una serie de revisiones de edición y formato.

```csharp
public static void Compare(string v1, string v2, string outputFileName, string author, 
    DateTime dateTime, CompareOptions compareOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| v1 | String | El documento original. |
| v2 | String | El documento modificado. |
| outputFileName | String | El nombre del archivo de salida. |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y hora que se utilizarán para las revisiones. |
| compareOptions | CompareOptions | Opciones de comparación de documentos. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo comparar documentos de forma sencilla.

```csharp
//Hay varias formas de comparar documentos:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Ver también

* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_2}

Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| v1 | String | El documento original. |
| v2 | String | El documento modificado. |
| outputFileName | String | El nombre del archivo de salida. |
| saveFormat | SaveFormat | Formato de guardado de la salida. |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y hora que se utilizarán para las revisiones. |
| compareOptions | CompareOptions | Opciones de comparación de documentos. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ejemplos

Muestra cómo comparar documentos de forma sencilla.

```csharp
//Hay varias formas de comparar documentos:
string firstDoc = MyDir + "Table column bookmarks.docx";
string secondDoc = MyDir + "Table column bookmarks.doc";

Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.1.docx", "Author", new DateTime());
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.2.docx", SaveFormat.Docx, "Author", new DateTime());

CompareOptions compareOptions = new CompareOptions();
compareOptions.IgnoreCaseChanges = true;
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.3.docx", "Author", new DateTime(), compareOptions);
Comparer.Compare(firstDoc, secondDoc, ArtifactsDir + "LowCode.CompareDocuments.4.docx", SaveFormat.Docx, "Author", new DateTime(), compareOptions);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Compare(*string, string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_3}

Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato.

```csharp
public static void Compare(string v1, string v2, string outputFileName, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| v1 | String | El documento original. |
| v2 | String | El documento modificado. |
| outputFileName | String | El nombre del archivo de salida. |
| saveOptions | SaveOptions | Opciones de guardado de la salida. |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y hora que se utilizarán para las revisiones. |
| compareOptions | CompareOptions | Opciones de comparación de documentos. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página se guardará como un archivo independiente. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte, siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare}

Compara dos documentos cargados desde secuencias con opciones adicionales y guarda las diferencias en la secuencia de salida proporcionada en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveFormat saveFormat, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| v1 | Stream | El documento original. |
| v2 | Stream | El documento modificado. |
| outputStream | Stream | El flujo de salida. |
| saveFormat | SaveFormat | Formato de guardado de la salida. |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y hora que se utilizarán para las revisiones. |
| compareOptions | CompareOptions | Opciones de comparación de documentos. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

## Ejemplos

Muestra cómo comparar documentos de la secuencia.

```csharp
// Hay varias formas de comparar documentos de la secuencia:
using (FileStream firstStreamIn = new FileStream(MyDir + "Table column bookmarks.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream secondStreamIn = new FileStream(MyDir + "Table column bookmarks.doc", FileMode.Open, FileAccess.Read))
    {
        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.1.docx", FileMode.Create, FileAccess.ReadWrite))
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime());

        using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.CompareStreamDocuments.2.docx", FileMode.Create, FileAccess.ReadWrite))
        {
            CompareOptions compareOptions = new CompareOptions();
            compareOptions.IgnoreCaseChanges = true;
            Comparer.Compare(firstStreamIn, secondStreamIn, streamOut, SaveFormat.Docx, "Author", new DateTime(), compareOptions);
        }
    }
}
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Compare(*Stream, Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, DateTime, [CompareOptions](../../../aspose.words.comparing/compareoptions/)*) {#compare_1}

Compara dos documentos cargados desde secuencias con opciones adicionales y guarda las diferencias en la secuencia de salida proporcionada en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato.

```csharp
public static void Compare(Stream v1, Stream v2, Stream outputStream, SaveOptions saveOptions, 
    string author, DateTime dateTime, CompareOptions compareOptions = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| v1 | Stream | El documento original. |
| v2 | Stream | El documento modificado. |
| outputStream | Stream | El flujo de salida. |
| saveOptions | SaveOptions | Opciones de guardado de la salida. |
| author | String | Iniciales del autor a utilizar para las revisiones. |
| dateTime | DateTime | La fecha y hora que se utilizarán para las revisiones. |
| compareOptions | CompareOptions | Opciones de comparación de documentos. |

## Observaciones

Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo se guardará la primera página de la salida en la secuencia especificada.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en la secuencia especificada.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* class [Comparer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
