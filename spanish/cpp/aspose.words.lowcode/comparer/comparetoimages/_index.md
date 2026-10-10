---
title: "Método CompareToImages de Aspose::Words::LowCode::Comparer"
linktitle: "CompareToImages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método CompareToImages de Aspose::Words::LowCode::Comparer. Compara dos documentos y guarda las diferencias como imágenes. Cada elemento en la matriz devuelta representa una sola página de la salida renderizada como una imagen en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.lowcode/comparer/comparetoimages/
---
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Compara dos documentos y guarda las diferencias como imágenes. Cada elemento en la matriz devuelta representa una sola página de la salida renderizada como una imagen.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | El documento original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | El documento modificado. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Las opciones de guardado de imagen de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compara dos documentos y guarda las diferencias como imágenes. Cada elemento en la matriz devuelta representa una sola página de la salida renderizada como una imagen.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | El documento original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | El documento modificado. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Las opciones de guardado de imagen de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) opciones de comparación. |

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) method


Compara dos documentos y guarda las diferencias como imágenes. Cada elemento en la matriz devuelta representa una sola página de la salida renderizada como una imagen.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::String\& | El documento original. |
| v2 | const System::String\& | El documento modificado. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Las opciones de guardado de imagen de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::CompareToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compara dos documentos y guarda las diferencias como imágenes. Cada elemento en la matriz devuelta representa una sola página de la salida renderizada como una imagen.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Comparer::CompareToImages(const System::String &v1, const System::String &v2, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &imageSaveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| v1 | const System::String\& | El documento original. |
| v2 | const System::String\& | El documento modificado. |
| imageSaveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Las opciones de guardado de imagen de la salida. |
| autor | const System::String\& | Iniciales del autor a usar para revisiones. |
| dateTime | System::DateTime | La fecha y hora a usar para las revisiones. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) opciones de comparación. |

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
