---
title: "Aspose::Words::LowCode::Replacer::Replace méthode"
linktitle: "Remplacer"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::LowCode::Replacer::Replace méthode. Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée en utilisant une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires en C++."
type: docs
weight: 1000
url: /fr/cpp/aspose.words.lowcode/replacer/replace/
---
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée en utilisant une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée en utilisant une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée en utilisant une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée en utilisant une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le flux d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::SharedPtr<System::IO::Stream> &inputStream, const System::SharedPtr<System::IO::Stream> &outputStream, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux d'entrée. |
| outputStream | const System::SharedPtr\<System::IO::Stream\>\& | Le flux de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), seule la première page de la sortie sera enregistrée dans le flux spécifié.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que TIFF multi‑images unique dans le flux spécifié.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée en utilisant une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée en utilisant une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, Aspose::Words::SaveFormat saveFormat, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveFormat | Aspose::Words::SaveFormat | Le format d'enregistrement. |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Enum [SaveFormat](../../../aspose.words/saveformat/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée en utilisant une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un modèle de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée en utilisant une expression régulière, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée, avec le format d'enregistrement spécifié et des options supplémentaires.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<Aspose::Words::Saving::SaveOptions> &saveOptions, const System::String &pattern, const System::String &replacement, const System::SharedPtr<Aspose::Words::Replacing::FindReplaceOptions> &options)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\& | Les options d'enregistrement. |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |
| options | const System::SharedPtr\<Aspose::Words::Replacing::FindReplaceOptions\>\& | Objet [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/) pour spécifier des options supplémentaires. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Class [FindReplaceOptions](../../../aspose.words.replacing/findreplaceoptions/)
* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée en utilisant une expression régulière.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::SharedPtr<System::Text::RegularExpressions::Regex> &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| motif | const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\& | Un motif d'expression régulière utilisé pour trouver des correspondances. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Replacer::Replace(const System::String\&, const System::String\&, const System::String\&, const System::String\&) method


Remplace toutes les occurrences d'un motif de chaîne de caractères spécifié par une chaîne de remplacement dans le fichier d'entrée.

```cpp
static int32_t Aspose::Words::LowCode::Replacer::Replace(const System::String &inputFileName, const System::String &outputFileName, const System::String &pattern, const System::String &replacement)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputFileName | const System::String\& | Le nom du fichier d'entrée. |
| outputFileName | const System::String\& | Le nom du fichier de sortie. |
| motif | const System::String\& | Une chaîne à remplacer. |
| remplacement | const System::String\& | Une chaîne pour remplacer toutes les occurrences du motif. |

### ReturnValue

Le nombre de remplacements effectués.
## Remarques


Si le format de sortie est une image (BMP, EMF, EPS, GIF, JPEG, PNG ou WebP), chaque page de la sortie sera enregistrée dans un fichier séparé. Le nom de fichier de sortie spécifié sera utilisé pour générer les noms de fichiers pour chaque partie selon la règle : outputFile_partIndex.extension.

Si le format de sortie est TIFF, la sortie sera enregistrée en tant que fichier TIFF multi‑images unique.

## Voir aussi

* Class [Replacer](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
