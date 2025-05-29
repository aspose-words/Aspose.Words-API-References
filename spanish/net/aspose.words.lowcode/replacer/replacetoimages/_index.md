---
title: Replacer.ReplaceToImages
linktitle: ReplaceToImages
articleTitle: ReplaceToImages
second_title: Aspose.Words para .NET
description: Transforme sin esfuerzo sus archivos de entrada reemplazando patrones de caracteres con cadenas personalizadas y generando imágenes impresionantes con nuestro método ReplaceToImages.
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/replacer/replacetoimages/
---
## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_2}

Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. Representa la salida en imágenes.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| pattern | String | Una cadena que debe reemplazarse. |
| replacement | String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

## Ejemplos

Muestra cómo reemplazar una cadena en el documento y guardar el resultado en imágenes.

```csharp
// Hay varias formas de reemplazar una cadena en el documento:
string doc = MyDir + "Footer.docx";
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

FindReplaceOptions options = new FindReplaceOptions();
options.FindWholeWordsOnly = false;
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages}

Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada. Representa la salida en imágenes.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string pattern, string replacement, FindReplaceOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| pattern | String | Una cadena que debe reemplazarse. |
| replacement | String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

## Ejemplos

Muestra cómo reemplazar una cadena en el documento usando documentos de la secuencia y guardar el resultado en imágenes.

```csharp
// Hay varias formas de reemplazar una cadena en el documento usando documentos del flujo:
string pattern = "(C)2006 Aspose Pty Ltd.";
string replacement = "Copyright (C) 2024 by Aspose Pty Ltd.";

using (FileStream streamIn = new FileStream(MyDir + "Footer.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);

    FindReplaceOptions options = new FindReplaceOptions();
    options.FindWholeWordsOnly = false;
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, options);
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ReplaceToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_3}

Reemplaza todas las ocurrencias de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. Representa la salida en imágenes.

```csharp
public static Stream[] ReplaceToImages(string inputFileName, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFileName | String | El nombre del archivo de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| pattern | Regex | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| replacement | String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

## Ejemplos

Muestra cómo reemplazar una cadena con expresiones regulares en el documento y guardar el resultado en imágenes.

```csharp
// Hay varias formas de reemplazar una cadena con una expresión regular en el documento:
string doc = MyDir + "Footer.docx";
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

Stream[] images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
images = Replacer.ReplaceToImages(doc, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## ReplaceToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Regex, string, [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)*) {#replacetoimages_1}

Reemplaza todas las ocurrencias de un patrón de expresión regular especificado con una cadena de reemplazo en el archivo de entrada. Representa la salida en imágenes.

```csharp
public static Stream[] ReplaceToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Regex pattern, string replacement, FindReplaceOptions options = null)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStream | Stream | El flujo de archivo de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| pattern | Regex | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| replacement | String | Una cadena para reemplazar todas las apariciones del patrón. |
| options | FindReplaceOptions | [`FindReplaceOptions`](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

## Ejemplos

Muestra cómo reemplazar una cadena con expresiones regulares en el documento usando documentos de la secuencia y guardar el resultado en imágenes.

```csharp
// Hay varias formas de reemplazar una cadena con una expresión regular en el documento usando documentos del flujo:
Regex pattern = new Regex("gr(a|e)y");
string replacement = "lavender";

using (FileStream streamIn = new FileStream(MyDir + "Replace regex.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement);
    images = Replacer.ReplaceToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), pattern, replacement, new FindReplaceOptions() { FindWholeWordsOnly = false });
}
```

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* class [Replacer](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
