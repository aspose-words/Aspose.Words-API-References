---
title: "Aspose::Words::LowCode::Converter::ConvertToImages método"
linktitle: "ConvertToImages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LowCode::Converter::ConvertToImages método. Convierte las páginas del documento especificado a imágenes en el formato especificado y devuelve una matriz de flujos que contienen las imágenes en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.lowcode/converter/converttoimages/
---
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) method


Convierte las páginas del documento especificado en imágenes en el formato especificado y devuelve una matriz de flujos que contienen las imágenes.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | El documento de entrada. |
| saveFormat | Aspose::Words::SaveFormat | Formato de guardado. Solo se permiten formatos de guardado de imagen. |

### ReturnValue

Devuelve una matriz de flujos de imagen. Los flujos deben ser eliminados por el usuario final.

## Ver también

* Class [Document](../../../aspose.words/document/)
* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convierte las páginas del documento especificado en imágenes usando las opciones de guardado especificadas y devuelve una matriz de flujos que contienen las imágenes.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<Aspose::Words::Document> &doc, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::Document\>\& | El documento de entrada. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opciones de guardado de imagen. |

### ReturnValue

Devuelve una matriz de flujos de imagen. Los flujos deben ser eliminados por el usuario final.

## Ver también

* Class [Document](../../../aspose.words/document/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Convierte las páginas del flujo de entrada especificado en imágenes en el formato especificado y devuelve una matriz de flujos que contienen las imágenes.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| saveFormat | Aspose::Words::SaveFormat | Formato de guardado. Solo se permiten formatos de guardado de imagen. |

### ReturnValue

Devuelve una matriz de flujos de imagen. Los flujos deben ser eliminados por el usuario final.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convierte las páginas del flujo de entrada especificado en imágenes usando las opciones de carga y guardado proporcionadas, y devuelve una matriz de flujos que contienen las imágenes.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Las opciones de carga del documento de entrada. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opciones de guardado de imagen. |

### ReturnValue

Devuelve una matriz de flujos de imagen. Los flujos deben ser eliminados por el usuario final.

## Ver también

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convierte las páginas del flujo de entrada especificado en imágenes usando las opciones de guardado especificadas y devuelve una matriz de flujos que contienen las imágenes.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opciones de guardado de imagen. |

### ReturnValue

Devuelve una matriz de flujos de imagen. Los flujos deben ser eliminados por el usuario final.

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, Aspose::Words::SaveFormat) method


Convierte las páginas del archivo de entrada especificado en imágenes en el formato especificado y devuelve una matriz de flujos que contienen las imágenes.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFile | const System::String\& | El nombre del archivo de entrada. |
| saveFormat | Aspose::Words::SaveFormat | Formato de guardado. Solo se permiten formatos de guardado de imagen. |

### ReturnValue

Devuelve una matriz de flujos de imagen. Los flujos deben ser eliminados por el usuario final.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convierte las páginas del archivo de entrada especificado en archivos de imagen usando las opciones de carga y guardado proporcionadas.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFile | const System::String\& | El nombre del archivo de entrada. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Las opciones de carga del documento de entrada. |
| outputFile | const System::String\& | El nombre de archivo de salida utilizado para generar el nombre de archivo de las imágenes de página usando la regla "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opciones de guardado de imagen. |

## Ver también

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convierte las páginas del archivo de entrada especificado en imágenes usando las opciones de guardado especificadas y devuelve una matriz de flujos que contienen las imágenes.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFile | const System::String\& | El nombre del archivo de entrada. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opciones de guardado de imagen. |

### ReturnValue

Devuelve una matriz de flujos de imagen. Los flujos deben ser eliminados por el usuario final.

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&) method


Convierte las páginas del archivo de entrada especificado en archivos de imagen.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFile | const System::String\& | El nombre del archivo de entrada. |
| outputFile | const System::String\& | El nombre de archivo de salida utilizado para generar el nombre de archivo de las imágenes de página usando la regla "outputFile_pageIndex.extension" |

## Ver también

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Convierte las páginas del archivo de entrada especificado en archivos de imagen en el formato especificado.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFile | const System::String\& | El nombre del archivo de entrada. |
| outputFile | const System::String\& | El nombre de archivo de salida utilizado para generar el nombre de archivo de las imágenes de página usando la regla "outputFile_pageIndex.extension" |
| saveFormat | Aspose::Words::SaveFormat | Formato de guardado. Solo se permiten formatos de guardado de imagen. |

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::ConvertToImages(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) method


Convierte las páginas del archivo de entrada especificado en archivos de imagen usando las opciones de guardado especificadas.

```cpp
static void Aspose::Words::LowCode::Converter::ConvertToImages(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFile | const System::String\& | El nombre del archivo de entrada. |
| outputFile | const System::String\& | El nombre de archivo de salida utilizado para generar el nombre de archivo de las imágenes de página usando la regla "outputFile_pageIndex.extension" |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Opciones de guardado de imagen. |

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
