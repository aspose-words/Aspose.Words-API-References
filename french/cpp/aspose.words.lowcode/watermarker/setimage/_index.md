---
title: "Aspose::Words::LowCode::Watermarker::SetImage méthode"
linktitle: "SetImage"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Watermarker::SetImage méthode. Ajoute un filigrane image dans le document à partir de flux avec des options en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.lowcode/watermarker/setimage/
---
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&) method


Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Image affichée comme filigrane. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Image affichée comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&) method


Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Flux d'image affiché comme filigrane. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Flux d'image affiché comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&) method


Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Image affichée comme filigrane. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Drawing::Image> &watermarkImage, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| watermarkImage | const System::SharedPtr\<System::Drawing::Image\>\& | Image affichée comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Flux d'image affiché comme filigrane. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane d'image dans le document à partir de flux avec des options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::IO::Stream> &watermarkImageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| watermarkImageStream | const System::SharedPtr\<System::IO::Stream\>\& | Flux d'image affiché comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&) method


Ajoute un filigrane d'image dans le document avec des options et le format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| watermarkImageFileName | const System::String\& | Image affichée comme filigrane. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane d'image dans le document avec des options et le format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| watermarkImageFileName | const System::String\& | Image affichée comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&) method


Ajoute un filigrane d'image dans le document avec des options et le format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| watermarkImageFileName | const System::String\& | Image affichée comme filigrane. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane d'image dans le document avec des options et le format d'enregistrement spécifié.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| watermarkImageFileName | const System::String\& | Image affichée comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&) method


Ajoute un filigrane d'image dans le document.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| watermarkImageFileName | const System::String\& | Image affichée comme filigrane. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Watermarker::SetImage(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Ajoute un filigrane d'image dans le document avec des options.

```cpp
static void Aspose::Words::LowCode::Watermarker::SetImage(const System::String &inputFileName, const System::String &outputFileName, const System::String &watermarkImageFileName, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| watermarkImageFileName | const System::String\& | Image affichée comme filigrane. |
| options | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Définit des options supplémentaires pour le filigrane image. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* Class [Watermarker](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
