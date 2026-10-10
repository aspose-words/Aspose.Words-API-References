---
title: "Aspose::Words::LowCode::Comparer::Compare méthode"
linktitle: "Compare"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Comparer::Compare méthode. Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni au format d'enregistrement spécifié, produisant des changements sous forme d'un nombre de révisions d'édition et de format en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.lowcode/comparer/compare/
---
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni au format d'enregistrement spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Le document original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Le document modifié. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni au format d'enregistrement spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Le document original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Le document modifié. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) options de comparaison. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni au format d'enregistrement spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Le document original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Le document modifié. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compare deux documents chargés à partir de flux avec des options supplémentaires et enregistre les différences dans le flux de sortie fourni au format d'enregistrement spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::SharedPtr<System::IO::Stream> &v1, const System::SharedPtr<System::IO::Stream> &v2, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::SharedPtr\<System::IO::Stream\>\& | Le document original. |
| v2 | const System::SharedPtr\<System::IO::Stream\>\& | Le document modifié. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) options de comparaison. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) method


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | Le document original. |
| v2 | const System::String\& | Le document modifié. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | Le document original. |
| v2 | const System::String\& | Le document modifié. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) options de comparaison. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) method


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | Le document original. |
| v2 | const System::String\& | Le document modifié. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié au format d'enregistrement fourni, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | Le document original. |
| v2 | const System::String\& | Le document modifié. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement de la sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) options de comparaison. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) method


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | Le document original. |
| v2 | const System::String\& | Le document modifié. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Comparer::Compare(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) method


Compare deux documents avec des options supplémentaires et enregistre les différences dans le fichier de sortie spécifié, produisant des modifications sous forme d'un nombre de révisions d'édition et de format.

```cpp
static void Aspose::Words::LowCode::Comparer::Compare(const System::String &v1, const System::String &v2, const System::String &outputFileName, const System::String &author, System::DateTime dateTime, const System::SharedPtr<Aspose::Words::Comparing::CompareOptions> &compareOptions)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| v1 | const System::String\& | Le document original. |
| v2 | const System::String\& | Le document modifié. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| auteur | const System::String\& | Initiales de l’auteur à utiliser pour les révisions. |
| dateTime | System::DateTime | La date et l'heure à utiliser pour les révisions. |
| compareOptions | const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\& | [Document](../../../aspose.words/document/) options de comparaison. |
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [CompareOptions](../../../aspose.words.comparing/compareoptions/)
* Class [Comparer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
