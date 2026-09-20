---
title: "Método Split de Aspose::Words::LowCode::Splitter"
linktitle: "Dividir"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Split de Aspose::Words::LowCode::Splitter. Divide un documento desde un flujo de entrada en múltiples partes según las opciones de división especificadas y devuelve las partes resultantes como una matriz de flujos en el formato de guardado especificado en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.lowcode/splitter/split/
---
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento de un flujo de entrada en múltiples partes según las opciones de división especificadas y devuelve las partes resultantes como una matriz de flujos en el formato de guardado especificado.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opciones de división. |

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento de un flujo de entrada en múltiples partes según las opciones de división especificadas y devuelve las partes resultantes como una matriz de flujos en el formato de guardado especificado.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Splitter::Split(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opciones de división. |

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento en múltiples partes según las opciones de división especificadas y guarda las partes resultantes en archivos en el formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre de archivo de salida utilizado para generar el nombre de archivo de las partes del documento usando la regla "outputFile_partIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opciones de división. |

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento en múltiples partes según las opciones de división especificadas y guarda las partes resultantes en archivos. El formato del archivo de salida se determina por la extensión del nombre del archivo de salida.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre de archivo de salida utilizado para generar el nombre de archivo de las partes del documento usando la regla "outputFile_partIndex.extension" |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opciones de división. |

## Ver también

* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Splitter::Split(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) method


Divide un documento en múltiples partes según las opciones de división especificadas y guarda las partes resultantes en archivos en el formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Splitter::Split(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<Aspose::Words::LowCode::SplitOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre de archivo de salida utilizado para generar el nombre de archivo de las partes del documento usando la regla "outputFile_partIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| options | const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\& | [Document](../../../aspose.words/document/) opciones de división. |

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [SplitOptions](../../splitoptions/)
* Class [Splitter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
