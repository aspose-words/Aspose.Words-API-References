---
title: Splitter.ExtractPages
linktitle: ExtractPages
articleTitle: ExtractPages
second_title: Aspose.Words para .NET
description: Extraiga fácilmente páginas específicas de cualquier documento con nuestro método Splitter ExtractPages. ¡Guárdelas en el formato que desee para acceder fácilmente!
type: docs
weight: 20
url: /es/net/aspose.words.lowcode/splitter/extractpages/
---
## ExtractPages(*string, string, int, int*) {#extractpages_4}

Extrae un rango específico de páginas de un archivo de documento y las guarda en un nuevo archivo. El formato del archivo de salida se determina por la extensión del nombre del archivo de salida.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, int startPageIndex, 
    int pageCount)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| startPageIndex | Int32 | El índice basado en cero de la primera página a extraer. |
| pageCount | Int32 | Número de páginas a extraer. |

## Ejemplos

Muestra cómo extraer páginas del documento.

```csharp
// Hay varias formas de extraer páginas del documento:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Ver también

* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages_2}

Extrae un rango específico de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo utilizando el formato de guardado especificado.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveFormat | SaveFormat | El formato de guardado. |
| startPageIndex | Int32 | El índice basado en cero de la primera página a extraer. |
| pageCount | Int32 | Número de páginas a extraer. |

## Ejemplos

Muestra cómo extraer páginas del documento.

```csharp
// Hay varias formas de extraer páginas del documento:
string doc = MyDir + "Big document.docx";

Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.1.docx", 0, 2);
Splitter.ExtractPages(doc, ArtifactsDir + "LowCode.ExtractPages.2.docx", SaveFormat.Docx, 0, 2);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ExtractPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_3}

Extrae un rango específico de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo utilizando el formato de guardado especificado.

```csharp
public static void ExtractPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions, int startPageIndex, int pageCount)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |
| startPageIndex | Int32 | El índice basado en cero de la primera página a extraer. |
| pageCount | Int32 | Número de páginas a extraer. |

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), int, int*) {#extractpages}

Extrae un rango específico de páginas de un flujo de documentos y guarda las páginas extraídas en un flujo de salida utilizando el formato de guardado especificado.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    int startPageIndex, int pageCount)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| outputStream | Stream | El flujo de salida. |
| saveFormat | SaveFormat | El formato de guardado. |
| startPageIndex | Int32 | El índice basado en cero de la primera página a extraer. |
| pageCount | Int32 | Número de páginas a extraer. |

## Ejemplos

Muestra cómo extraer páginas del documento desde la secuencia.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ExtractPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.ExtractPages(streamIn, streamOut, SaveFormat.Docx, 0, 2);
}
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ExtractPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), int, int*) {#extractpages_1}

Extrae un rango específico de páginas de un flujo de documentos y guarda las páginas extraídas en un flujo de salida utilizando el formato de guardado especificado.

```csharp
public static void ExtractPages(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    int startPageIndex, int pageCount)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| outputStream | Stream | El flujo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |
| startPageIndex | Int32 | El índice basado en cero de la primera página a extraer. |
| pageCount | Int32 | Número de páginas a extraer. |

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
