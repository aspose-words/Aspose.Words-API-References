---
title: Splitter.RemoveBlankPages
linktitle: RemoveBlankPages
articleTitle: RemoveBlankPages
second_title: Aspose.Words para .NET
description: Elimina fácilmente las páginas vacías de tus documentos con el método RemoveBlankPages de Splitter. ¡Ahorra tiempo y optimiza tu flujo de trabajo hoy mismo!
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/splitter/removeblankpages/
---
## RemoveBlankPages(*string, string*) {#removeblankpages_2}

Elimina las páginas vacías del documento y guarda el resultado. Devuelve una lista de los números de página eliminados.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |

### Valor_devuelto

La lista de números de página se consideró en blanco y se eliminó.

## Ejemplos

Muestra cómo eliminar páginas vacías del documento.

```csharp
// Hay varias formas de eliminar páginas vacías del documento:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Ver también

* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages_3}

Elimina las páginas vacías del documento y guarda la salida en el formato especificado. Devuelve una lista de los números de página eliminados.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveFormat | SaveFormat | El formato de guardado. |

### Valor_devuelto

La lista de números de página se consideró en blanco y se eliminó.

## Ejemplos

Muestra cómo eliminar páginas vacías del documento.

```csharp
// Hay varias formas de eliminar páginas vacías del documento:
string doc = MyDir + "Blank pages.docx";

Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.1.docx");
Splitter.RemoveBlankPages(doc, ArtifactsDir + "LowCode.RemoveBlankPages.2.docx", SaveFormat.Docx);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## RemoveBlankPages(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_4}

Elimina las páginas vacías del documento y guarda la salida en el formato especificado. Devuelve una lista de los números de página eliminados.

```csharp
public static List<int> RemoveBlankPages(string inputFileName, string outputFileName, 
    SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| outputFileName | String | El nombre del archivo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |

### Valor_devuelto

La lista de números de página se consideró en blanco y se eliminó.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#removeblankpages}

Elimina las páginas en blanco de un documento proporcionado en un flujo de entrada y guarda el documento actualizado en un flujo de salida con el formato de guardado especificado. Devuelve una lista de los números de página eliminados.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveFormat saveFormat)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| outputStream | Stream | El flujo de salida. |
| saveFormat | SaveFormat | El formato de guardado. |

### Valor_devuelto

La lista de números de página se consideró en blanco y se eliminó.

## Ejemplos

Muestra cómo eliminar páginas vacías del documento desde la secuencia.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Blank pages.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.RemoveBlankPagesStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Splitter.RemoveBlankPages(streamIn, streamOut, SaveFormat.Docx);
}
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## RemoveBlankPages(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#removeblankpages_1}

Elimina las páginas en blanco de un documento proporcionado en un flujo de entrada y guarda el documento actualizado en un flujo de salida con el formato de guardado especificado. Devuelve una lista de los números de página eliminados.

```csharp
public static List<int> RemoveBlankPages(Stream inputStream, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de entrada. |
| outputStream | Stream | El flujo de salida. |
| saveOptions | SaveOptions | Las opciones de guardado. |

### Valor_devuelto

La lista de números de página se consideró en blanco y se eliminó.

### Ver también

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Splitter](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
