---
title: "Aspose::Words::LowCode::Comparer::Compare método"
linktitle: "Compare"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LowCode::Comparer::Compare método. Compara dos documentos cargados desde flujos con opciones adicionales y guarda las diferencias en el flujo de salida proporcionado en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Compara dos documentos cargados desde flujos con opciones adicionales y guarda las diferencias en el flujo de salida proporcionado en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | El documento original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | El documento modificado. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compara dos documentos cargados desde flujos con opciones adicionales y guarda las diferencias en el flujo de salida proporcionado en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | El documento original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | El documento modificado. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) opciones de comparación. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Compara dos documentos cargados desde flujos con opciones adicionales y guarda las diferencias en el flujo de salida proporcionado en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | El documento original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | El documento modificado. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compara dos documentos cargados desde flujos con opciones adicionales y guarda las diferencias en el flujo de salida proporcionado en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | El documento original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | El documento modificado. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) opciones de comparación. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::String\& | El documento original. |
| v2 | const System::String\& | El documento modificado. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::String\& | El documento original. |
| v2 | const System::String\& | El documento modificado. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) opciones de comparación. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::String\& | El documento original. |
| v2 | const System::String\& | El documento modificado. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::String\& | El documento original. |
| v2 | const System::String\& | El documento modificado. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) opciones de comparación. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::String\& | El documento original. |
| v2 | const System::String\& | El documento modificado. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado, produciendo cambios como una serie de revisiones de edición y formato.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::String\& | El documento original. |
| v2 | const System::String\& | El documento modificado. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) opciones de comparación. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
