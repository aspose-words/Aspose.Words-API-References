---
title: "Método ExtractPages de Aspose::Words::LowCode::Splitter"
linktitle: "ExtractPages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método ExtractPages de Aspose::Words::LowCode::Splitter. Extrae un rango especificado de páginas de un flujo de documento y guarda las páginas extraídas en un flujo de salida usando el formato de guardado especificado en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.lowcode/splitter/extractpages/
---
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extrae un rango especificado de páginas de un flujo de documento y guarda las páginas extraídas en un flujo de salida usando el formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| startPageIndex | int32_t | El índice basado en cero de la primera página a extraer. |
| pageCount | int32_t | Número de páginas a extraer. |

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Extrae un rango especificado de páginas de un flujo de documento y guarda las páginas extraídas en un flujo de salida usando el formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| startPageIndex | int32_t | El índice basado en cero de la primera página a extraer. |
| pageCount | int32_t | Número de páginas a extraer. |

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) method


Extrae un rango especificado de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo usando el formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, int32_t startPageIndex, int32_t pageCount)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| startPageIndex | int32_t | El índice basado en cero de la primera página a extraer. |
| pageCount | int32_t | Número de páginas a extraer. |

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) method


Extrae un rango especificado de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo usando el formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, int32_t startPageIndex, int32_t pageCount)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| startPageIndex | int32_t | El índice basado en cero de la primera página a extraer. |
| pageCount | int32_t | Número de páginas a extraer. |

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::ExtractPages(const System::String\&, const System::String\&, int32_t, int32_t) method


Extrae un rango especificado de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo. El formato del archivo de salida se determina por la extensión del nombre del archivo de salida.

```cpp
static void Aspose::Words::LowCode::Splitter::ExtractPages(const System::String &inputFileName, const System::String &outputFileName, int32_t startPageIndex, int32_t pageCount)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| startPageIndex | int32_t | El índice basado en cero de la primera página a extraer. |
| pageCount | int32_t | Número de páginas a extraer. |

## Ver también

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
