---
title: "Aspose::Words::LowCode::Watermarker::SetImage método"
linktitle: "SetImage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LowCode::Watermarker::SetImage método. Añade una marca de agua de imagen al documento desde flujos con opciones en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.lowcode/watermarker/setimage/
---
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) method


Agrega una marca de agua de imagen al documento desde flujos con opciones.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Imagen que se muestra como marca de agua. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento desde flujos con opciones.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) method


Agrega una marca de agua de imagen al documento desde flujos con opciones.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Flujo de imagen que se muestra como marca de agua. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento desde flujos con opciones.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Flujo de imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) method


Agrega una marca de agua de imagen al documento desde flujos con opciones.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Imagen que se muestra como marca de agua. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento desde flujos con opciones.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Agrega una marca de agua de imagen al documento desde flujos con opciones.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Flujo de imagen que se muestra como marca de agua. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento desde flujos con opciones.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de entrada. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Flujo de imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), solo la primera página de la salida se guardará en el flujo especificado.

Si el formato de salida es TIFF, la salida se guardará como un único TIFF de varios fotogramas en el flujo especificado.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Agrega una marca de agua de imagen al documento con opciones y formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| watermarkImageFileName | const System::String\& | Imagen que se muestra como marca de agua. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento con opciones y formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveFormat | Aspose::Words::SaveFormat | El formato de guardado. |
| watermarkImageFileName | const System::String\& | Imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Agrega una marca de agua de imagen al documento con opciones y formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| watermarkImageFileName | const System::String\& | Imagen que se muestra como marca de agua. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento con opciones y formato de guardado especificado.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Las opciones de guardado. |
| watermarkImageFileName | const System::String\& | Imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&) method


Agrega una marca de agua de imagen al documento.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| watermarkImageFileName | const System::String\& | Imagen que se muestra como marca de agua. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento con opciones.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFileName | const System::String\& | El nombre del archivo de entrada. |
| outputFileName | const System::String\& | El nombre del archivo de salida. |
| watermarkImageFileName | const System::String\& | Imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |
## Observaciones


Si el formato de salida es una imagen (BMP, EMF, EPS, GIF, JPEG, PNG o WebP), cada página de la salida se guardará como un archivo separado. El nombre de archivo de salida especificado se utilizará para generar los nombres de archivo de cada parte siguiendo la regla: outputFile_partIndex.extension.

Si el formato de salida es TIFF, la salida se guardará como un único archivo TIFF de varios fotogramas.

## Ver también

* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
