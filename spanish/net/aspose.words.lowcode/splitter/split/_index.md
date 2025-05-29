---
title: Splitter.Split
linktitle: Split
articleTitle: Split
second_title: Aspose.Words para .NET
description: Divide fácilmente tus documentos en varias secciones con nuestro flexible método Splitter Split. ¡Guarda en tu formato preferido para una gestión de archivos sencilla!
type: docs
weight: 40
url: /es/net/aspose.words.lowcode/splitter/split/
---
## Split(*string, string, [SplitOptions](../../splitoptions/)*) {#split_2}

Divide un documento en varias partes según las opciones de división especificadas y guarda las partes resultantes en archivos. El formato del archivo de salida se determina por la extensión del nombre del archivo de salida.

```csharp
public static void Split(string inputFileName, string outputFileName, SplitOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida utilizado para generar el nombre de archivo de las partes del documento mediante la regla "outputFile_partIndex.extension" |
| options | SplitOptions | Opciones de división de documentos. |

## Ejemplos

Muestra cómo dividir el documento por páginas.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Ver también

* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Split(*string, string, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split_3}

Divide un documento en varias partes según las opciones de división especificadas y guarda las partes resultantes en archivos en el formato de guardado especificado.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    SplitOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida utilizado para generar el nombre de archivo de las partes del documento mediante la regla "outputFile_partIndex.extension" |
| saveFormat | SaveFormat | El formato de guardado. |
| options | SplitOptions | Opciones de división de documentos. |

## Ejemplos

Muestra cómo dividir el documento por páginas.

```csharp
string doc = MyDir + "Big document.docx";

SplitOptions options = new SplitOptions();
options.SplitCriteria = SplitCriteria.Page;
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.1.docx", options);
Splitter.Split(doc, ArtifactsDir + "LowCode.SplitDocument.2.docx", SaveFormat.Docx, options);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Split(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_4}

Divide un documento en varias partes según las opciones de división especificadas y guarda las partes resultantes en archivos en el formato de guardado especificado.

```csharp
public static void Split(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    SplitOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida utilizado para generar el nombre de archivo de las partes del documento mediante la regla "outputFile_partIndex.extension" |
| saveOptions | SaveOptions | Las opciones de guardado. |
| options | SplitOptions | Opciones de división de documentos. |

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Split(*Stream, [SaveFormat](../../../aspose.words/saveformat/), [SplitOptions](../../splitoptions/)*) {#split}

Divide un documento de un flujo de entrada en varias partes según las opciones de división especificadas y devuelve las partes resultantes como una matriz de flujos en el formato de guardado especificado.

```csharp
public static Stream[] Split(Stream inputStream, SaveFormat saveFormat, SplitOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| saveFormat | SaveFormat | El formato de guardado. |
| options | SplitOptions | Opciones de división de documentos. |

## Ejemplos

Muestra cómo dividir el documento del flujo por páginas.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    SplitOptions options = new SplitOptions();
    options.SplitCriteria = SplitCriteria.Page;
    Stream[] stream = Splitter.Split(streamIn, SaveFormat.Docx, options);
}
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## Split(*Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), [SplitOptions](../../splitoptions/)*) {#split_1}

Divide un documento de un flujo de entrada en varias partes según las opciones de división especificadas y devuelve las partes resultantes como una matriz de flujos en el formato de guardado especificado.

```csharp
public static Stream[] Split(Stream inputStream, SaveOptions saveOptions, SplitOptions options)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| saveOptions | SaveOptions | Las opciones de guardado. |
| options | SplitOptions | Opciones de división de documentos. |

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [SplitOptions](../../splitoptions/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
