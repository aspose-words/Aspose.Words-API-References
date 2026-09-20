---
title: "Método Replace de Aspose::Words::LowCode::Replacer"
linktitle: "Replace"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Replace de Aspose::Words::LowCode::Replacer. Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el flujo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.lowcode/replacer/replace/
---
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el flujo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el flujo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el flujo de entrada, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el flujo de entrada, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el flujo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el flujo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el flujo de entrada, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el flujo de entrada, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las ocurrencias de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada, con el formato de guardado especificado y opciones adicionales.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) objeto para especificar opciones adicionales. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada usando una expresión regular.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| patrón | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un patrón de expresión regular utilizado para encontrar coincidencias. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::String\&, const System::String\&) method


Reemplaza todas las apariciones de un patrón de cadena de caracteres especificado con una cadena de reemplazo en el archivo de entrada.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::String &pattern, const System::String &replacement)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| patrón | const System::String\& | Una cadena a ser reemplazada. |
| reemplazo | const System::String\& | Una cadena para reemplazar todas las apariciones del patrón. |

### ReturnValue

El número de reemplazos realizados.
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
