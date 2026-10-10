---
title: "Aspose::Words::LowCode::Splitter::RemoveBlankPages método"
linktitle: "RemoveBlankPages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LowCode::Splitter::RemoveBlankPages método. Elimina páginas en blanco de un documento proporcionado en un flujo de entrada y guarda el documento actualizado en un flujo de salida en el formato de guardado especificado. Devuelve una lista de números de página que fueron eliminados en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.lowcode/splitter/removeblankpages/
---
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Elimina páginas en blanco de un documento proporcionado en un flujo de entrada y guarda el documento actualizado en un flujo de salida en el formato de guardado especificado. Devuelve una lista de números de página que fueron eliminados.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |

### ReturnValue

La lista de números de página se ha considerado en blanco y se ha eliminado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Elimina páginas en blanco de un documento proporcionado en un flujo de entrada y guarda el documento actualizado en un flujo de salida en el formato de guardado especificado. Devuelve una lista de números de página que fueron eliminados.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |

### ReturnValue

La lista de números de página se ha considerado en blanco y se ha eliminado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&) method


Elimina páginas vacías del documento y guarda la salida. Devuelve una lista de números de página que fueron eliminados.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |

### ReturnValue

La lista de números de página se ha considerado en blanco y se ha eliminado.

## Ver también

* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Elimina páginas vacías del documento y guarda la salida en el formato especificado. Devuelve una lista de números de página que fueron eliminados.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |

### ReturnValue

La lista de números de página se ha considerado en blanco y se ha eliminado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::RemoveBlankPages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Elimina páginas vacías del documento y guarda la salida en el formato especificado. Devuelve una lista de números de página que fueron eliminados.

```cpp
static System::SharedPtr<System::Collections::Generic::List<int32_t>> Aspose::Words::LowCode::Splitter::RemoveBlankPages(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |

### ReturnValue

La lista de números de página se ha considerado en blanco y se ha eliminado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
