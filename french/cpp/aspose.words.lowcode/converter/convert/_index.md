---
title: "Méthode Convert de Aspose::Words::LowCode::Converter"
linktitle: "Convertir"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Convert de Aspose::Words::LowCode::Converter. Convertit le document d'entrée fourni en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.lowcode/converter/convert/
---
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Convertit le document d'entrée donné en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Les flux d'entrée. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Les options de chargement du document d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) method


Convertit le document d'entrée donné en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Convertit le document d'entrée donné en un seul document de sortie en utilisant les flux d'entrée et de sortie spécifiés.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Les flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés ainsi que ses options de chargement/enregistrement.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Les options de chargement du document d'entrée. |
| outputFile | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&) method


Convertit le document d’entrée fourni en document de sortie en utilisant les noms de fichiers d’entrée et de sortie spécifiés ainsi que leurs extensions.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| outputFile | const System::String\& | Le nom du fichier de sortie. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) method


Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et le format final du document.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, Aspose::Words::SaveFormat saveFormat)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| outputFile | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Converter::Convert(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) method


Convertit le document d'entrée donné en document de sortie en utilisant les noms de fichiers d'entrée et de sortie spécifiés et les options d'enregistrement.

```cpp
static void Aspose::Words::LowCode::Converter::Convert(const System::String &inputFile, const System::String &outputFile, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFile | const System::String\& | Le nom du fichier d'entrée. |
| outputFile | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Converter](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
